# Deliverable 2

## How to install Proxmox VE
1. Download the Proxmox VE ISO from the official website.  
2. Flash the ISO to a USB drive using Rufus.  
3. Boot your computer from the USB drive.  
4. Select **Install Proxmox VE**.  
5. Accept the license agreement.  
6. Choose the storage drive for installation.  
7. Set the administrator password and network settings.  
8. Complete the installation and reboot.  
9. Access the web interface:  
   **https://YOUR-SERVER-IP:8006 (proxmox default port)**

---

## How to create a Debian container
1. In Proxmox, go to **Node → CT Templates**.  
2. Download a **Debian** template (example: Debian 12).  
3. Click **Create CT**.  
4. Set:
   - **Hostname**  
   - **Password**  
5. Select the Debian template you downloaded.  
6. Choose disk size, CPU cores, and RAM.  
7. Set the network to **DHCP** (or static).  
8. Finish and start the container.

---

## How to install MariaDB
Run the following commands inside the Debian container:

```sh
apt update
apt install mariadb-server -y

