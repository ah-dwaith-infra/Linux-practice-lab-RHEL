Task 1 — Verify System Information

Before starting your work, verify:

Which user is currently logged in
```
whoami
```
Your current working directory
```
pwd
```
The current system date
```
date
```
Task 2 — Navigate to the Project Workspace

Go to your home directory.
```
cd
```
Navigate to the project directory.
```
mkdir project
cd project
```
Confirm you are inside the correct directory.
```
pwd
```
Inside your project directory, the final structure should look like this:
project
│
├── logs
│   ├── app.log
│   ├── error.log
│
├── config
│   ├── app.conf
│   ├── db.conf
│
├── data
│   ├── users.txt
│   └── inventory.txt
│
└── notes.txt
```
mkdir -p project/logs/app.log project/logs/error.log project/config/app.conf project/config/db.conf project/data/users.txt project/data/inventory.txt project/notes.txt
```
```
tree project
```
After creating the files, add some sample content so you can practice text commands.

logs/app.log

Example entries:
Server started successfully
Application initialized
Database connection established
User login successful
```
echo "Server started successfully
Application initialized
Database connection established
User login successful" >> project/logs/app.log
```

logs/error.log

Example entries:
Error: Connection timeout
Error: Database unreachable
Warning: Disk space low
Error: Timeout while contacting API
```
echo "Error: Connection timeout
Error: Database unreachable
Warning: Disk space low
Error: Timeout while contacting API" >> /project/logs/error.log
```

config/app.conf
APP_NAME=InventorySystem
APP_PORT=8080
LOG_LEVEL=INFO
```
echo "APP_NAME=InventorySystem
APP_PORT=8080
LOG_LEVEL=INFO" >> app.cong
```

config/db.conf
DB_HOST=localhost
DB_PORT=3306
DB_NAME=inventory
```
echo "DB_HOST=localhost
DB_PORT=3306
DB_NAME=inventory" >> db.conf
```

data/users.txt
Alice
Bob
Charlie
David
Emma
```
echo "Alice
Bob
Charlie
David
Emma" >> users.txt
```

data/inventory.txt
Laptop
Keyboard
Mouse
Monitor
Printer
```
echo "Laptop
Keyboard
Mouse
Monitor
Printer" >> inventory.txt
```

notes.txt
Project setup notes
Initial configuration completed
Logs need monitoring
```
echo "Project setup notes
Initial configuration completed
Logs need monitoring" >> notes.txt
```

Task 3 — Inspect Directory Structure

List all files in the project directory.
```
ls -ll
```
Display inode numbers for the files.
```
ls -li
```
View the entire directory structure.
```
tree project
```
Display the contents of app.log.
```
cat app.log
```
Display the contents of error.log.
```
cat error.log
```
Open app.log using a pager to read it comfortably.
```
more app.log
```

Task 5 — Analyze Log Data

Count the number of lines in app.log.
```
wc -l app.log
```
Count the number of words in error.log.
```
wc -w error.log
```
Display the first 2 lines of app.log.
```
head -2 app.log
```
Display the last 2 lines of error.log.
```
tail -2 app.log
```

Task 6 — Search Logs

Search error.log for the word timeout.
```
grep -i "timeout" error.log
```
Search for the word Error in the log files.
```
grep -i "error" app.log error.log
```
Search inside the project directory for any line containing Database.
```
grep -i "database" /root/project/
```

Task 8 — Move Configuration Files

Create a directory called configs_backup.
```
mkdir configs_backup
```
Move all configuration files there.
```
mv /root/project/config /root/project/configs_backup
```
Verify the directory.
```
ls -ll
```

Task 9 — Create File Links

Create a hard link to app.log.
```
ln /root/project/logs/app.log /root/project/logs/app_hard.log
```
Create a symbolic link to app.log.
```
ln -s /root/project/logs/app.log /root/project/logs/app_soft.log
```
Compare inode numbers.
```
ls -li
```

Task 10 — File Discovery

Find all .log files inside the project directory.
```
find / -name "*.log"
```
Find all .conf files.
```
find / -name "*.conf"
```
