--------------------------------------------------------------------------------------------------------------
There are 2 files in the homedirectory: passwords.old and passwords.new. 
The password for the next level is in passwords.new 
and is the only line that has been changed between passwords.old and passwords.new
--------------------------------------------------------------------------------------------------------------


ssh -i sshkey.private bandit17@bandit.labs.overthewire.org -p 2220

diff passwords.old passwords.new

>> x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
