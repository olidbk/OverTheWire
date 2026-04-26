--------------------------------------------------------------------------------------------------------------
The password for the next level is stored in the file data.txt, which contains base64 encoded data
--------------------------------------------------------------------------------------------------------------


sshpass -f "sshpass" ssh bandit10@bandit.labs.overthewire.org -p 2220

base64 -d data.txt 

>> dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
