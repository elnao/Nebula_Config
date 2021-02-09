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

