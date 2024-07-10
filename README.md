# OpenVPN Access Server Installation Guide

This README file provides a step-by-step guide for setting up OpenVPN Access Server on an Ubuntu 22.04.4 LTS system.

## Prerequisites

1. **SSH Access**: Ensure you have SSH access to your server.
2. **Root Privileges**: You need root access to install and configure OpenVPN Access Server.

## Steps

### 1. Set Permissions for the SSH Key

```bash
chmod 600 key.pem
```

### 2. Connect to the Server via SSH

```bash
ssh -i key.pem root@["domain-name/ip address"]
```

### 3. Update the System

Update the package lists and upgrade the system packages:

```bash
sudo apt update
sudo apt upgrade -y
```

### 4. Add OpenVPN Access Server Repository

Add the OpenVPN Access Server repository to your system:

```bash
echo "deb [signed-by=/etc/apt/keyrings/openvpn-as.gpg.key] http://as-repository.openvpn.net/as/debian $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/openvpn-as.list
```

### 5. Add the Repository GPG Key

Download and add the GPG key for the OpenVPN Access Server repository:

```bash
wget --quiet -O - https://as-repository.openvpn.net/as-repo-public.gpg | sudo tee /etc/apt/keyrings/openvpn-as.gpg.key
```

### 6. Install Required Packages

Ensure apt-transport-https and ca-certificates packages are installed:

```bash
sudo apt install apt-transport-https ca-certificates -y
```

### 7. Update Package Lists

Update the package lists again to include the OpenVPN repository:

```bash
sudo apt update
```

### 8. Install OpenVPN Access Server

Install the OpenVPN Access Server package:

```bash
sudo apt install -y openvpn-as
```

### 9. Access the OpenVPN Access Server Web UI

Once the installation is complete, access the Admin and Client UIs using the following URLs:

- Admin UI: https://64.227.170.44:943/admin
- Client UI: https://64.227.170.44:943/

### 10. Login to the Admin UI

Use the "openvpn" account with the default password provided during installation. You can change the password via the Admin UI.

## Step1:

- ### Go to the url and enter cerendials:

![alt text](<images/Screenshot 2024-07-10 153211.png>)

- ### Download OpenVpn Client Application:

![alt text](<images/Screenshot 2024-07-10 153227.png>)

- ### Steps in Installation of OpenVpn Client Application:

![alt text](<images/Screenshot 2024-07-10 153315.png>)
![alt text](<images/Screenshot 2024-07-10 153538.png>)
![alt text](<images/Screenshot 2024-07-10 153627.png>)
![alt text](<images/Screenshot 2024-07-10 153640.png>)
![alt text](<images/Screenshot 2024-07-10 153653.png>)
![alt text](<images/Screenshot 2024-07-10 153754.png>)

- ### OpenVpn Connect:

![alt text](<images/Screenshot 2024-07-10 153717.png>)
![alt text](<images/Screenshot 2024-07-10 153731.png>)
![alt text](<images/Screenshot 2024-07-10 153744.png>)

## Your new Ipv4 Address:

![alt text](<images/Screenshot 2024-07-10 132757.png>)
