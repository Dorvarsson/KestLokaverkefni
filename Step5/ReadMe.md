- Ran the command: "sudo apt install bind9"
- Configured the file: "/etc/bind/named.conf.local" so it used the correct domain name (hostdo.local)
![Step5-Server-named conf local](https://github.com/user-attachments/assets/f9c13b5a-6af8-4f71-88fa-f3d1750ca0a0)
- Ran the command: "sudo systemctl restart bind9"
- Ran the command: "sudo systemctl status bind9" to verify the status of the server
- Ran the command "nslookup server1.hostdo.local" on the client to test the connection
- Ran the command "ping server1.hostdo.local" on the client to test the connection
