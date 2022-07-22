# RDC-Debian
## Remote Desktop Connection from a Windows machine to Debian based linux machine.

### 1) Install xrdp.
`sudo apt install xrdp -y`

### 2) Start and enable xrdp.
`sudo systemctl start xrdp`<br />
`sudo systemctl enable xrdp`

### 3) Check the status of xrdp.
`sudo systemctl status xrdp`

### 4) Add xrdp to ssl-cert group.
`sudo adduser xrdp ssl-cert`

### 5) Restart xrdp.
`sudo systemctl restart xrdp`

### 6) Install ufw (it is usually already installed by default).
`sudo apt install ufw`

### 7) Check ufw status (usually disabled by default).
`sudo ufw status`

### 8) Enable ufw if neccessary.
`sudo ufw enable`

### 9) Allow port 3389/tcp which is needed for RDC.
`sudo ufw allow 3389/tcp`

### 10) Check firewall status. You should see that it is enabled and allows connection over port 3389/tcp from anywhere.
`sudo ufw status`

### 11) Check your Linux machine IP.
`ip a`<br />
or<br />
`ifconfig`

### 11) On you Windows machine, type _rdc_ in start menu, enter your Linux machine IP. A new window will open. Log in with your Linux username and password. 
