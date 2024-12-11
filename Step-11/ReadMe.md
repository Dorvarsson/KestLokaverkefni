- Ran the command: "sudo apt install opanssh-server"
- Configured the file "/etc/ssh/sshd_config" so it placed the groups IT and Stjornun in AllowedGroups
![Step11-Server-sshd_config](https://github.com/user-attachments/assets/ade78d5b-819b-4ec8-9c28-a5d601b0a532)

- Ran the command: "sudo systemctl restart ssh"
- Ran the command: "ssh Gus@192.168.1.1" from the user Gus to test
