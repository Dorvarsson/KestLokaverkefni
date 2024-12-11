- Ran the command: "sudo apt install samba"
- Ran the command: "sudo mkdir -p /samba/{IT,Sala,Stjornun}" to create directories for every group
![Step9-Server-samba](https://github.com/user-attachments/assets/37f8b182-cfde-44c9-ba68-e25d0918fa36)

### These commands were used to set ownership and permissions for everygroups directory
- sudo chown root:IT /samba/IT
- sudo chown root:Sala /samba/Sala
- sudo chown root:Stjornun /samba/Stjornun
- sudo chmod 2770 /samba/IT
- sudo chmod 2770 /samba/Sala
- sudo chmod 2770 /samba/Stjornun
#
- Configured the file "/etc/samba/smb.conf" to setup new samba shared directories
![Step9-Server-smb conf](https://github.com/user-attachments/assets/b532816b-6b0e-447e-b5fb-c53a8bc44b6e)
- Ran the command: "sudo systemctl restart smbd"
- Ran the command: "sudo systemctl enable smbd" to active to service
- Ran the command: "ls /samba/It" on a user that didnt have permission to test permission
- Ran the command: "sudo smbpasswd -a <users username>" for every user

### These commands were used to give the IT and Stjornum groups full access to all shared directories
- sudo setfacl -m g:IT:rwx /samba/IT
- sudo setfacl -m g:IT:rwx /samba/Sala
- sudo setfacl -m g:IT:rwx /samba/Stjornun
- sudo setfacl -m g:Stjornun:rwx /samba/IT
- sudo setfacl -m g:Stjornun:rwx /samba/Sala
- sudo setfacl -m g:Stjornun:rwx /samba/Stjornun

- Ran the command: "getfacl /samba/IT" to check the ACL, I then did the same with the other groups
