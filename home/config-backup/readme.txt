---
In case of a system reset over-writing config files that we have customised
copy the files from /root/config-backup as follows

cp /root/config-backup/rc.local /etc/rc.d/rc.local
cp /root/config-backup/crontab /etc/cron.d/crontab
cp /root/config-backup/interfaces /etc/network/interfaces
cp /root/config-backup/localtime /etc/locatime
---

The script /root/bin/set-time-ntp is run at boot time and (via a cron job)
on the hour to sync the system time to a network time server. The server
that it uses may need changing in the script depending on where the system
is used. The cron job saves details of the offset to /root/logs/set-time.log

The clock drift is typically ~0.03s per hour, less than 1 sample interval at 
20Hz.

