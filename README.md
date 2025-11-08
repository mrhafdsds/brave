One-Click Brave Docker on VPS

Run a full-featured Brave browser securely inside Docker on any VPS with just one script.
Access it from your browser with VNC-over-web and login authentication.

📦 Features
🔐 Secure browser access via password
🐳 Docker + Docker Compose auto-installed
🔥 UFW Firewall auto-configured (only required ports allowed)
🌐 Access Brave from anywhere (web-based UI)
💻 SSH remains open on port 22
🚀 Quick Start for single brave without proxy
SSH into your VPS

Install Dependencies

bash

Copy code
sudo apt update && sudo apt install curl -y
Download and run the script:
bash

Copy code
bash <(curl -sL https://raw.githubusercontent.com/mrhafdsds/brave/main/setup_brave.sh)
🚀 Quick Start for multiple brave multiple proxy
SSH into your VPS

Install Dependencies

bash

Copy code
sudo apt update && sudo apt install curl -y
Download and run the script:
bash

Copy code
bash <(curl -sL https://raw.githubusercontent.com/mrhafdsds/brave/main/multi_brave.sh)
You will be asked for a username and password use these later to log in to the browser interface.

Access the Browser
After the script completes, open this URL in your browser:


Copy code
http://<your-vps-ip>:4100
Login with the username/password you provided.

Ports Used
Port

Purpose

4100

Web-based Brave UI

4101

Internal VNC socket

22

SSH (still open)

Security Notes
UFW is auto-enabled with only ports 22, 4100, and 4101 allowed.
To change allowed IPs, edit UFW:
bash

Copy code
ufw allow from <your-ip> to any port 4100
Requirements
Ubuntu/Debian-based VPS
Root access
💬 Questions? Join Telegram
