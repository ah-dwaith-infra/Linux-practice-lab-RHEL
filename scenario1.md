# RHEL Practice Lab 1

## Objective
Practice basic Linux file management, searching, and command usage.

---

## Task 1: Check Environment

Check the following:

1. Display the current logged-in user.

Answer: whoami

2. Display the current working directory.

Answer: pwd

3. Display today's date.

Answer: date 

## Task 2: Directory Creation

Create the following directory structure inside your home directory.

projectX
projectX/docs
projectX/data
projectX/logs

Answer: mkdir -p projectX/docs projectX/data projectX/logs 

## Task 3: File Creation

Inside the docs directory create these files:

report.txt
notes.txt
summary.txt

Answer:cd docs 
        touch report.txt notes.txt summary.txt

## Task 4: Add Content

Add the following lines to report.txt

Server started
Phoenix Project running
Backup completed
DevOps team

Answer: echo "Server started
Phoenix Project running
Backup completed
DevOps team" >> report.txt

## Task 5: File Operations

1. Copy report.txt to the data directory.

Answer: cp -r /home/projectX/docs/report.txt /home/projectX/data/

2. Rename notes.txt to ideas.txt

Answer:mv /home/projectX/docs/notes.txt/ /home/projectX/docs/ideas.txt

## Task 6: Links

1. Create a hard link for report.txt named report_hard.txt

Answer: ln /home/projectX/docs/report.txt /home/projectX/docs/report_hard.txt

2. Create a symbolic link named report_soft.txt

Answer: ln -s /home/projectX/docs/report.txt /home/projectX/docs/repost_soft.txt

## Task 7: File Analysis

1. Display the first 2 lines of report.txt

Answer:head -2 report.txt 

2. Display the last line of report.txt

Answer:tail -1 report.txt

3. Count the number of lines in report.txt

Answer: wc -l report.txt

## Task 8: Search

1. Find lines containing the word "Project"

Answer:grep -i "project" report.txt

2. Find lines starting with "Server"

Answer:grep -i "^server" report.txt

3. Find lines ending with "team"

Answer:grep -i "team$" report.txt

## Task 9: Find Files

1. Find report.txt inside your home directory.

Answer:find /home -name report.txt

2. Find directories named docs.

Answer:find / -type d -name docs 

