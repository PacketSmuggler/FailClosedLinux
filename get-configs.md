
You're going to need one working Cryptostorm config file, but we'll pull all of them to get things set up. They are stored here:

https://github.com/cryptostorm/cryptostorm_client_configuration_files

So you'll do this to get a copy:

git clone https://github.com/cryptostorm/cryptostorm_client_configuration_files.git

Assuming you start in your home directory, the files we need will end up in ~/cryptostorm_client_configuration_files/linux

Change into that directory and you're going to use the findhosts and mkhost command that are part of this repository. They scan the ovpn files and create an 'etchosts' file, which you can append to your actual /etc/hosts file.

Linux users with some knowledge often as why we're doing this at this point in the process. We're going to thwart DNS leaks from the virtual machine by blocking DNS with ipchains, but that'll happen AFTER we have our /etc/host file the way we want it.
