# 🚀 n8n Auto Installer

A fully automated installation script for **n8n**, using **Docker**, **Nginx reverse proxy**, and **Let's Encrypt SSL**.  
Deploy n8n on your server with just **one command**.

[🇮🇷 Read in Persian (Farsi)](README.fa.md)

---

## ⭐ Features
- One-click installation of n8n  
- Full Docker installation + auto configuration  
- Nginx reverse proxy with WebSocket support  
- Automatic SSL (Let's Encrypt + Certbot)  
- Works on Ubuntu 20.04 / 22.04 / 24.04  
- Persistent n8n data using Docker volumes  
- Clean and readable Bash script  

---

## 📦 Requirements
- Ubuntu server (20+ recommended)
- A domain pointing to the server’s IP (A Record)
- Root or sudo privileges
- Port 80 and 443 must be open  

---

## 📥 Download the Script
```bash
wget https://raw.githubusercontent.com/USERNAME/n8n-auto-installer/main/install.sh
chmod +x install.sh
```

---

## ⚙️ How to Install

### 1. Run the installer  
Replace **yourdomain.com** with your actual domain:

```bash
sudo ./install.sh yourdomain.com
```

---

## 🧩 What the Script Automatically Does
- Updates the system  
- Installs Docker, Nginx, Certbot  
- Pulls and runs the n8n Docker container  
- Creates persistent Docker volume  
- Generates Nginx reverse proxy configuration  
- Enables WebSocket support for n8n  
- Issues an HTTPS certificate using Let's Encrypt  
- Reloads Nginx automatically  

---

## 📁 Project Structure
```
/
├── install.sh
└── README.md
```

---

## 📝 Important Notes
- Update the email inside the script for SSL:
```bash
--email your_email@example.com
```

- Make sure your domain DNS A-Record is correctly pointing to your server before installation.

---

## 🔒 Security
- Full HTTPS setup  
- Correct Nginx headers  
- WebSocket compatibility  
- Automatic SSL renewal included via Certbot  

---

## 🧪 Uninstall / Reinstall
To remove old containers before reinstalling:

```bash
docker stop n8n
docker rm n8n
docker volume rm n8n_data
```

---

## 🤝 Contributing
Contributions and pull-requests are welcome!  
Feel free to open issues for bugs, improvements, or suggestions.

---

## ⭐ Support
If this project helped you, please give it a **star** ⭐ on GitHub!

---

## 📜 License
MIT License
