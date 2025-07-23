# Project: Initial Ubuntu Server Setup & Hardening

* **Objective:** To perform a clean installation of Ubuntu Server, update it, and apply baseline security measures to harden the OS.

---

### Steps Taken

1.  **Installation:**
    * Flashed Ubuntu Server 22.04 LTS image to a USB drive.
    * Installed the OS with a minimal package set.
    * Configured a static IP address for the server.

2.  **Initial Updates:**
    * Ran `sudo apt update` and `sudo apt upgrade -y` to bring all packages up to date.

3.  **User Management:**
    * Created a new non-root user for daily administration.
    * Added the user to the `sudo` group to grant administrative privileges.
    * Disabled the root account login over SSH.

4.  **Firewall Configuration:**
    * Enabled UFW (Uncomplicated Firewall).
    * Set the default policy to deny all incoming traffic.
    * Allowed incoming traffic only for SSH (port 22).
    * **Command used:** `sudo ufw allow ssh`

### Challenges & Solutions

* **Challenge:** I initially forgot to open the SSH port in the firewall before enabling it, locking myself out.
* **Solution:** Had to connect a monitor and keyboard directly to the server to log in locally and run `sudo ufw allow ssh`. A great lesson in thinking through firewall rules before applying them!
