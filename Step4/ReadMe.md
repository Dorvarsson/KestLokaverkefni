- Ran the command: "sudo apt install isc-dhcp-server"
- Configured the file: "/etc/dhcp/dhcpd.conf" so it used the correct ip address
![Step4-Server-dhcpd conf](https://github.com/user-attachments/assets/cac27e74-1b01-4dae-be57-619d0b7df822)
- Configured the file: "/etc/default/isc-dhcp-server" so that it used the correct ethernet connection(ens37)
![Step4-Server-isc-dhcp-server](https://github.com/user-attachments/assets/22a09487-5ecc-4e66-a6ac-e0bdb608b304)
- Ran the command: "sudo systemctl restart isc-dhcp-server"
- Ran the command: "sudo systemctl status isc-dhcp-server" to verify the status of the server
