- Ran the command: "sudo apt install apache2"
- Ran the command: "sudo apt install openssl"
- Ran the command: "sudo mkdir /etc/apach2/ssl" to create the dictionary ssl
- Ran the command: "sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/apache2/ssl/apache.key -out /etc/apache2/ssl/apache.crt" to create a certificate and a key
- Created the file "/etc/apach2/sites-available/hostdo.local.conf"
- Ran the command: "sudo a2dissite default-ssl" to disable the default ssl site
![Step12-Server-hostdo local-ssl conf](https://github.com/user-attachments/assets/d17e447f-e662-44f2-a745-d7f33b957ad8)

- Ran the command: "sudo a2ensite hostdo.local.conf" to enable the new ssl site
- Ran the command: "sudo systemctl restart apach2"
- Configured the file "" on the client to allow the client to access the website
![Step12-Client-Hosts](https://github.com/user-attachments/assets/74773c83-7e72-4365-a0c6-23b8eb318ba7)

- Tested the website by accessing it with "https://hostdo.local"

