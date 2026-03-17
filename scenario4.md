Task 1 — Create Website Structure

Inside the project directory, create the following structure:

A directory for website files

A directory for logs

A directory for backups
```
mkdir -p project/webfiles project/logs project/backups
```

Task 2 — Create Website Files

Inside the website directory:
```
cd /root/project/webfiles/
```
Create:

A homepage file

A styles file

A script file 
```
touch homepage.txt styles.txt script.sh
```
```
ls -ll
```
Add some sample content into each file.
```
echo "beginning of homepage" >> homepage.txt
echo "beginning of styles" >> styles.txt
echo "beginning of script" >> script.sh
```

Task 3 — Verify File Contents

Display the contents of all website files.
```
cat homepage.txt styles.txt script.txt
```
Open at least one file using a pager for better readability.
```
less script.sh
```

Task 4 — Simulate Log Generation

Inside the logs directory:
```
cd /root/project/logs/
```
Create a log file.
```
touch system.log
```
Add multiple entries such as:
"Server started
Page accessed
Error messages"
```
echo "Server started
Page accessed
Error messages" >> system.log
```

Task 5 — Analyze Logs

Count:
Number of lines
```
wc -l system.log
```
Number of words
```
wc -w system.log
```
View:
First few entries
```
head -2 system.log
```
Last few entries
```
tail -2 system.log
```
Task 6 — Search Website Activity

Search logs for:
The word Error
```
grep -i "error" system.log
```
Search logs for:
The word accessed
```
grep -i "accessed" system.log
```

Task 7 — Create Backup

Copy the entire website directory into the backup directory.
```
cp -r /root/projects/webfiles/ /root/projects/backups/
```
Verify that the backup exists.
```
cd backups ; ls -ll
```

Task 8 — Rename and Move Files

Rename one of the website files.
```
mv /root/projects/webfiles/homepage.txt /root/projects/webfiles/header.txt
```
Move one file to another directory.
```
mv /root/projects/webfiles/header.txt /root/projects/backups/
```
Verify the changes.
```
cd backups ; ls -ll
```

Task 9 — Create Links for Quick Access

Create a shortcut (link) to the homepage file.
```
ln -s /root/project/webfiles/header.txt /root/project/webfiles/header_soft.txt
```
Verify that the link works correctly.
```
ls -li
```

Task 10 — Locate Website Files

Find all files related to the website (e.g., specific extensions).
```
find / -name "*.txt"
```
Display their locations.
```
find . -name "*.txt"
```
