This is a connection which allows you to run command shells securely through the internet. Before connecting to a server you must know the servers IP Address, and or Domain Name (DNS), as well as the username you wish to connect as in the server.
``` bash 
ssh username@serverhost
```
# SSH Keys
To identify yourself and other servers, you will use a key pair of public and private keys. 
* Your public key will be displayed to the entire world, and or the server you're trying to interact with. It will be used to encrypt messages sent to you.
* Your private key will decrypt messages that were encrypted by your public key.
## Generating Key Pairs
To generate these private and public key pairs, you use a program called `ssh-keygen` which uses special encryption algorithms to produce them. According to the [Arch Linux wiki](https://wiki.archlinux.org/title/SSH_keys) the default currently as of December 20th, 2025, is **Ed25519**. That said you can tweak it using the `-t` parameter. An example would be 
``` bash
ssh-keygen -t rsa
```
To increase the amount of bits in encryption, you can specify it using the `-b` option
``` bash
ssh-keygen -t rsa -b 4096
```
## Sharing SSH Public Keys
To share keys generated using `ssh-keygen` you use `ssh-copy-id`
## Config Files
The format for config files starts with you specifying a shortcut for when you run a command in the config file. Within it you are given a long list of options, for ease of use in maneuvering various ssh servers. To encode the command `ssh username@serverhost -p 222` you can do:
``` config
Host dev
	HostName serverhost
	User username
	Port 222
```
and just run `ssh dev`. For all options go to the [wiki](https://man.openbsd.org/OpenBSD-current/man5/ssh_config.5).