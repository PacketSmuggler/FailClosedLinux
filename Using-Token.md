
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

The string after the equal sign is your hash, this is used as the USERNAME in your Cryptostorm setup.

