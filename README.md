# scp-secure-copy-protocol

scp uses AES-128 encryption by default. and also uses PORT 22 to securely transfer files between 2 servers.  
Both cipher algorithm and port can be changed using parameters in scp command.

scp -c [new-cipher-algo] file1.txt raju@destination_host_ip:destination_folder_path

https://www.tecmint.com/scp-commands-examples/
https://linuxize.com/post/how-to-use-scp-command-to-securely-transfer-files/
https://www.softwaretestinghelp.com/scp-command-tutorial/
