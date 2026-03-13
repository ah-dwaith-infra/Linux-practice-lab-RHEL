Task 1 – Create the Investigation Workspace

Go to your home directory.

Create this directory structure:

investigation/
├── logs
├── reports
└── backup

Verify the structure using a command that shows directory trees.

```
cd root 
```
```
pwd
```
```
mkdir -p investigation/logs investigation/reports  investigation/backup
```
```
tree investigation
```

Create Sample Log Files

Inside the logs directory create three files:

access.log
error.log
system.log

Add the following content using echo and redirection.

```
cd logs
```
```
touch access.log error.log system.log
'''
Add the following content using echo and redirection.
(access.log)
INFO User login success
INFO File uploaded
ERROR Invalid request
INFO Session created
WARNING Slow response
(error.log)
ERROR Database connection failed
ERROR Permission denied
WARNING Disk almost full
INFO Retry successful
(system.log)
INFO System boot
INFO Service started
WARNING High CPU usage
ERROR Memory allocation failed
INFO System stable


```
echo "INFO User login success
INFO File uploaded
ERROR Invalid request
INFO Session created
WARNING Slow response" >> access.log
```
```
echo"ERROR Database connection failed
ERROR Permission denied
WARNING Disk almost full
INFO Retry successful" >> error.log
```
```
echo "INFO System boot
INFO Service started
WARNING High CPU usage
ERROR Memory allocation failed
INFO System stable" >> system.log
```

Task 3 – Log Inspection

Use commands to investigate logs.

View the first 3 lines of access.log.

View the last 2 lines of system.log.

Count how many lines exist in error.log.

Count how many words exist in access.log.


```
head -3 access.log
```
```
tail -2 system.log
```
```
wc -l error.log
```
```
wc -w access.log
```

Task 4 – Search for Problems

Use grep.

Find all lines containing ERROR in the logs directory.

Find WARNING messages only from system.log.

Save all ERROR messages into a new file:
reports/errors_report.txt

```
grep -i "error" system.log error.log access.log >> /root/invistigation/reports/error_report.txt
```
```
grep -i "warning" system.log >> /root/invistigation/reports/error_report.txt
```


Task 5 – Combine Commands (Pipes Practice)

Use pipes (|).

Show the number of ERROR messages across all logs.

Show only ERROR lines but display them with less.

```
grep -i "error" system.log error.log access.log | wc -l 
```
```
grep -i "error" system.log error.log access.log | less
```

Task 6 – Backup Logs

Copy the entire logs directory into the backup directory.

Verify the copy using tree.

```
cp -r  /root/investigation/logs/ /root/investigation/backup/
```
```
tree investigation
```

Task 7 – Create a Symbolic Link

Create a symbolic link in your home directory called:

latest_logs

that points to:

~/investigation/logs

Verify the link using ls -li.

```
ln -s /root/invistigation/logs/ /root/latest_logs
```
```
ls -li
```

Task 8 – File Discovery

Using find:

Find all .log files inside the investigation directory.

Find files containing the word error.

```
find investigation -name "*.log"
```
```
grep -i "error" /investigation/logs/* 
```



