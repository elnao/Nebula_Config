# Nebula_Config
Config files and reminders on how to re-setup Nebula networking.

Customize config.yml to point to the 3 certificates that you created for this device.

Copy 3 certificate files and customized config.yml to /opt/nebula
wget latest version of nebula.  Note, Raspberry Pi 3B+ uses ARM7 Architecture, and Raspberry P Zero sues ARM6 Architecture

## Install Service on Linux
Copy nebula.service file to /etc/systemd/system
Then run the below 2 commands
`sudo systemctl start nebula`
`sudo systemctl enable nebula`

## iOS App Config
1. Install Nebula app on iOS device
2. Click **+**
3. Click **Certificate**
4. Click **Generate Keys**
5. Click **Share Public Key**.   **STAY ON THIS SECREEN IN THE NEBULA APP**
6. Email key (device.pub) to yourself so you can get in on the same computer that you are going to run **Nebula_Cert.exe** on. 
7. In Windows copy the deivce.pub file to `C:\Program Files\Nebula`.
8. Copy your ca.key file into `C:\Program Files\Nebula`.
9. In PowerShell Admin run `./nebula-cert sign -in-pub device.pub -name "Iphone" -ip "10.XXX.XXX.XXX/24"`
10. Copy the newly created *Iphone.crt* and your *ca.crt* to your iPhone.  I used Google Drive.
11. Back in the Nebula app on your iPhone, click on the **File** option.
12. Click **Choose a file**.
13. Select the *Iphone.crt* file. Save
14. Click **CA**
15. Click the **File** option.
16. Click **Choose a file**
17. Select the *ca.crt* file. Save
18. Click **Hosts**
19. Under **Nebula IP**, type the internal Ip address of your Lighthouse server.
20. Turn *ON* the **Lighthouse** Selector
21. Under **List of public IPs or dns names where for this host** enter the public IP of your Lighthouse server with a port of 4242.
22. **Save**
23. Go back to the main screen of your new Nebula network, and turn the **Status** selector *ON*.
24. Hopefully you are now on your Nebula network.

