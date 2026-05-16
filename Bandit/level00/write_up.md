--------------------------------------------------------------------------------------------------------------
"
The password for the next level is stored in a file called readme located in the home directory. 
Use this password to log into bandit1 using SSH. 
Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.
"
--------------------------------------------------------------------------------------------------------------


# you can use 'sshpass' instead of 'ssh' and save the password level in a file

sshpass -f "sshpass" ssh bandit0@bandit.labs.overthewire.org -p 2220

cat readme

>> ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
