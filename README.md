# Arch Linux Setup Configuration
This repository contains a collection of configuration files and setup instructions for configuring an Arch Linux system. It includes setup for SSH, nftables, and other essential configurations. This setup is based on and extends the configurations from:

## Features
SSH: Configuration to disable root login for enhanced security.
nftables: Configuration for firewall with nft-blackhole to block unwanted traffic.
General Arch Linux Setup: Includes additional useful configurations for a secure and efficient system.

### Prerequisites
Arch Linux installation (base system).
Basic understanding of Linux command line and Arch Linux setup.

### Setup SSH:
Disable Root Login:
Edit the SSH configuration file to disable root login:
```sh
sudo nano /etc/ssh/sshd_config
```
Uncomment or add the following line:
```
PermitRootLogin no
```
Restart SSH Service:
```sh
sudo systemctl restart sshd
```

### Install nftables:

```sh
sudo pacman -S nftables
```

Apply Basic nftables Configuration:
Copy the nftables configuration file to /etc/nftables.conf:
```sh
sudo cp nftables.conf /etc/nftables.conf
```

### Enable and Start nftables:
```sh
sudo systemctl enable nftables
sudo systemctl start nftables
```


### System Updates: Regularly update the system using:
```sh
sudo pacman -Syu
```

Backup: Regularly back up your important files and configuration files.
Security: Ensure that your system is secure by regularly reviewing and updating security configurations and practices.
