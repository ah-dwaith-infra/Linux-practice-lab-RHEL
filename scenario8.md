Phase 1 — Identity Check
Verify your current user identity
Confirm you are operating as the correct administrative user
```
whoami
```

🔹 Phase 2 — Create Department Groups
Create the following groups:
engineering
testing
```
groupadd engineering ; groupadd testing
```
Verify that both groups exist
```
tail -3 /etc/group/
```

Phase 3 — Onboard Users

Create the following users:

Engineering Team
eng1
eng2
```
useradd eng1 ;useradd eng2
```
Testing Team
test1
test2
```
useradd test1
useradd test2
```
Temporary Contractor
contractor
```
useradd contractor
```

Phase 4 — Set User Passwords
Set passwords for all users created
Ensure each account is accessible
```
passwd eng1
passwd eng2
passwd test1
passwd test2
passwd contractor
```

Phase 5 — Access Verification
Switch into:
One engineering user
One testing user
```
su - eng1
su - test1
```
For each user:
Verify identity
```
id eng1
id test1
```
Observe environment differences between su and su -
Return to your original user
```
logout / exit
```

Phase 6 — Validate User Information
Check identity details for:
eng1
test1
contractor
Confirm:
Users exist
They have unique identities
```
id eng1
id test1
id contractor
```

Phase 7 — Temporary Access Removal
The contractor's work is complete
Remove:
contractor
Ensure:
The account is completely removed
Associated data is also removed
```
userdel -r contractor
```

Phase 8 — Team Restructure
Testing team is no longer needed
Remove:
test1
test2
Remove the testing group
```
userdel -r test1 ; userdel -r test2
groupdel testing
```

Phase 9 — Final Validation
Verify:
eng1 and eng2 still exist
engineering group still exists
Confirm removed users/groups are no longer present
```
tail -5 /etc/passwd
tail -5 /etc/group
```
