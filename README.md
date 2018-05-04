# csf-update-check
Small script to manually check for CSF upgrades and send out a e-mail notification if there is an update available. CSF has only auto-updates so if you disable that you don't get notified for new versions. 

## Create log file folder
```
cd /root
mkdir update-logs/csf
```
## Copy script
Copy the script to
```
cd /root
mkdir update-scripts
cd update-scripts
mkdir csf
cd csf
nano csf-update-check.sh
chmod 700 csf-update-check.sh
```

## Enable crontab
```
crontab -e
```
Example:
```
# CSF UPDATE CHECK
41 0 * * * /root/update-scripts/csf-update-check.sh > /dev/null 2>&1
```

Done! :)
