--------------------------------------------------------------------------------------------------------------
The password for the next level is stored somewhere on the server and has all of the following properties:
owned by user bandit7
owned by group bandit6
33 bytes in size
--------------------------------------------------------------------------------------------------------------


sshpass -f "sshpass" ssh bandit6@bandit.labs.overthewire.org -p 2220

find / -type f -user "bandit7" -group "bandit6" -size 33c 2>/dev/null

cat /var/lib/dpkg/info/bandit7.password

>> morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
