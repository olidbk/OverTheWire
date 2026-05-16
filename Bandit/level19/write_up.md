-----------------------------------------------------------------------------------------------------------------
"
To gain access to the next level, you should use the setuid binary in the homedirectory. 
Execute it without arguments to find out how to use it. 
The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.
"
-----------------------------------------------------------------------------------------------------------------


sshpass -f "sshpass" ssh bandit19@bandit.labs.overthewire.org -p 2220

ls -lah

# we see that the file is a setuid file, that's means we can act as another user when we run the script

./bandit20-do whoami

>> bandit20

./bandit20-do cat /etc/bandit_pass/bandit20

>> 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
