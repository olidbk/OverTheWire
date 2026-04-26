--------------------------------------------------------------------------------------------------------------
The credentials for the next level can be retrieved by submitting the password of the current level 
to a port on localhost in the range 31000 to 32000. 
First find out which of these ports have a server listening on them. 
Then find out which of those speak SSL/TLS and which don’t. 
There is only 1 server that will give the next credentials, 
the others will simply send back to you whatever you send to it.
--------------------------------------------------------------------------------------------------------------


sshpass -f "sshpass" ssh bandit16@bandit.labs.overthewire.org -p 2220

cat /etc/bandit_pass/bandit16

>> kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

nmap -sV -p31000-32000 localhost

>> 31790/tcp open  ssl/unknown

echo "kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx" | openssl s_client -connect localhost:31790 -ign_eof

# then he will give you a ssh privat key you need to copy it and past it in a file.
# then change his permetion with 'chmod 600 'file_name''
