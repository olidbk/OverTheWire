--------------------------------------------------------------------------------------------------------------
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once
--------------------------------------------------------------------------------------------------------------


sshpass -f "sshpass" ssh bandit8@bandit.labs.overthewire.org -p 2220

sort data.txt | uniq -u

>> 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
