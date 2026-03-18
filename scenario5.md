Task 1 — Create Workspace

Create a directory called workspace
Inside it, create:
A directory for documents
A directory for logs
```
mkdir -p workspace/docs workspace/logs
```
Task 2 — Create and Add Content

Inside the documents directory:

Create a file called notes.txt
Add at least 3 lines of content
```
touch notes.txt
```
```
echo "line1
line2
line3" >> notes.txt
```

Inside the logs directory:

Create a file called activity.log
Add at least 3 entries (mix of normal + error messages)
```
touch activity.log
```
```
echo " line1
syntax error
context error" >> activity.log
```

Task 3 — Inspect and Analyze

Display the contents of both files

View:
First few lines
Last few lines
```
head -2 notes.txt
tail -2 notes.txt
```
```
head -2 activity.log
tail -2 activity.log
```
Count:
Number of lines in each file
```
wc -l notes.txt
```
```
wc -l activity.log
```

Task 4 — Search and Verify

Search the log file for the word:
Error
```
grep -i "error" activity.log
```

Search the workspace for the word:
line1
```
grep -i "line1" notes.txt
```

Task 5 — Backup Workspace

Create a directory called backup
```
mkdir backup
```
Copy the entire workspace into it
```
cp -r /root/workspace/ /root/backup/
```
Verify that the backup was created
```
cd backup ; ls -ll
```

Goal of This Lab

Creating everything from zero
File handling
Content verification
Searching
Backup
