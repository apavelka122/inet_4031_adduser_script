# inet_4031_adduser_script

## INET4031 Add Users Script and User List

### Program Description
The `inet_4031_adduser_script` is a Python script designed to automate user account creation on a Linux server. The script reads from an input file (`create-users.input`) containing user information, then processes each line to create user accounts, assign passwords, and add users to specified groups. This is especially useful for system administrators who need to add multiple users across different servers efficiently.

### Program Operation
To use this script, follow these steps:

1. **Prepare the Input File**  
   Ensure `create-users.input` contains user details in the correct format:
- Each field is separated by a colon (`:`).
- Multiple groups should be separated by commas, and a dash (`-`) can be used to skip group assignment.

2. **Set Permissions**  
Ensure the script has execute permissions. Use this command:
```bash
chmod +x create-users.py
sudo ./create-users.py < create-users.input
   # Examples:
user1:password123:Smith:John:admin,staff
user2:password456:Doe:Jane:-
user3:password789:Brown:Mike:staff
