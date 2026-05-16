--------------------------------------------------------------------------------------------------------------
"
The password for the next level is stored in a file somewhere under the inhere directory. 
And has all of the following properties:
human-readable
1033 bytes in size
not executable
"
--------------------------------------------------------------------------------------------------------------


sshpass -f "sshpass" ssh bandit5@bandit.labs.overthewire.org -p 2220

cd inhere

find . -type f -readable -not -executable -size 1033c

cat ./maybehere07/.file2

>> HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
