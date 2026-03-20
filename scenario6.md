Task 1 — Create Health Check Structure

Create a directory called healthcheck
Inside it, create:
A directory for logs
A directory for reports
```
mkdir -p healthcheck/logs healthcheck/reports
```

Task 2 — Simulate System Logs

Inside the logs directory:
Create a file called system.log
Add at least 4 entries, including:
Normal messages
At least one error message
```
echo "system turned on 
systemchecked
system functioning 
system cooling system on 
storage error 
runtime error" >> system.log
```

Task 3 — Generate a Report

Inside the reports directory:
Create a file called daily_report.txt
Add at least 3 lines summarizing system status
```
echo "system up and running 
system active 
colling system functioning 
runnning status turn on 
30s start up time taken" >> daily_report.txt
```

Task 4 — Inspect and Analyze

View contents of both files

Display:
First few lines
Last few lines
```
head -2 system.log
tail -2 system.log
```
```
head -2 daily_report.txt
tail -2 daily_report.txt
```

Count:
Number of lines in system.log
```
wc -l system.log
```

Task 5 — Search for Issues

Search the logs for the word:
Error
```
grep -ri "error" /root/healthchek/logs/
``` 
Search the entire healthcheck directory for the word:
system
```
grep -ri "system" /root/healthcheck/
```

Task 6 — Create Quick Access Link

Create a shortcut (link) to the system.log file in the main healthcheck directory
Verify that the link works
```
ln -s /root/healthcheck/logs/system.log /root/healthcheck/
```
```
ls -li
```

Task 7 — Backup the Setup

Create a directory called hc_backup
```
mkdir hc_backup
```
Copy the entire healthcheck directory into it
```
cp -r /root/healthcheck/ /root/hc_backup/
```
Verify the backup structure
```
tree hc_backup
```



(scenario trained for ,
Working from empty system ,
File + directory creation ,
Log simulation ,
Text analysis ,
Searching ,
Links ,
Backup . )
