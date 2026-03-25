Task 1 — Verify Current User
Check your current user details
```
id root
```
Confirm your identity before making changes
```
whoami
```

Task 2 — Create Team Group
Create a group called developers
```
groupadd developers
```

Task 3 — Create Users
Create the following users:
dev1
dev2
tempuser
```
useradd dev1
useradd dev2
useradd tempuser
```
Set passwords for all users
```
passwd dev1
passwd dev2
passwd tempuser
```

Task 4 — Switch and Verify Users
Switch to dev1
```
su - dev1
```
Verify the user identity
```
whoami
```
Switch back to your original user
```
logout or exit
```

Task 5 — Clean Up Temporary User
Delete the user tempuser
Ensure:
The user is completely removed
Their home directory is also deleted
```
uderdel -r tempuser
```

Task 6 — Remove Group
Delete the developers group
Verify it has been removed
```
groupdel developers
```
```
tail -5 /etc/group/
```

