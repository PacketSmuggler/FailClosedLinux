
When you receive your token it will look something like this:

EkX4T-5S6ix-AfMYC-zvFy6

You can determine the SHA512 hash of your token by doing this:

cat > token
EkX4T-5S6ix-AfMYC-zvFy6
ctrl-d

then

openssl dgst -sha512 token

and for the sample it will return this:

SHA512(token)= aaf1cfde9ca47db5f68e1a9b3679d9105643e0b5200592d40cb03d6c0ed58e89460186082d47974bb9c09a825c4b0ca69ffdafa540f4e1ca2a9562a2d4018f81

The string after the equal sign is your hash, this is your proof of purchase. This is used as the USERNAME for Cryptostorm. There is no specific PASSWORD to go with it, but OpenVPN requires a PASSWORD. The following code sequence will do everything you need EXCEPT the final step of modifying the ovpn file itself.

cat > token
EkX4T-5S6ix-AfMYC-zvFy6
ctrl-d

openssl dgst -sha512 token | awk -F " " {'print $2'} > /etc/openvpn/pass.txt
echo "whatever" >> /etc/openvpn/pass.txt

Once you've got a two line file /etc/openvpn/pass.txt, where the first line is a token's hash, and the second is non-empty, you need to find the following line in /etc/openvpn/whatever-node-youre-using.ovpn

auth-user-pass

and change it to

auth-user-pass pass.txt



