# scp-secure-copy-protocol

scp uses AES-128 encryption by default. and also uses PORT 22 to securely transfer files between 2 servers.  
Both cipher algorithm and port can be changed using parameters in scp command.

scp -c [new-cipher-algo] file1.txt raju@destination_host_ip:destination_folder_path

By Default SCP uses AES-128 bit cipher, to encrypt and send the file from source to destination.  
However it can be configured to use any available cipher, using the scp -c parameter. 

Source:      VM1(10.55.64.xx) 
Destination: VM2(10.55.64.xx).
File name:   Smoke_2mins.mp4

Login into source VM and issue below commands.

RUSER='r00498@unxxx.enxxx'            [User ID of Destination Host]
HOST=10.55.64.XX                      [Destination Host's IP]
DIR=/home/R00498/Desktop/Code/gstreamer/         [Directory where you want to save the file in Host] 

scp -o user=$RUSER /home/R00498/Desktop/video/FireAndSmoke_6mins.mp4 $HOST:$DIR

This will then prompt to enter the password for the host system.  Once you enter file will be transferred instantly.
If you configure SSH Key based authentication, then it will login without having to enter password.

Copy files between 2 remote servers:
scp [user]@[remote_host]:[remote_file_path] [user]@[remote_host]:[remote_dir]

Copy from remote server to Local Machine:
scp [user]@[remote_host]:[remote_file_path] [local_dir]


https://www.tecmint.com/scp-commands-examples/
https://linuxize.com/post/how-to-use-scp-command-to-securely-transfer-files/
https://www.softwaretestinghelp.com/scp-command-tutorial/
