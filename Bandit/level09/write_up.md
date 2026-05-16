--------------------------------------------------------------------------------------------------------------
"
The password for the next level is stored in the file data.txt in one of the few human-readable strings, 
preceded by several ‘=’ characters.
"
--------------------------------------------------------------------------------------------------------------


sshpass -f "sshpass" ssh bandit9@bandit.labs.overthewire.org -p 2220

strings data.txt | grep "==="

>> FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
