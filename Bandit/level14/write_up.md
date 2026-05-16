--------------------------------------------------------------------------------------------------------------
"
The password for the next level can be retrieved by submitting the password of the current level 
to port 30000 on localhost.
"
--------------------------------------------------------------------------------------------------------------


ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220

# to take the password of the current level

cat /etc/bandit_pass/bandit14

>> MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

echo "MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS" | nc -v localhost 30000

>> 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
