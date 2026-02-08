# 🖥️ Predator Aurora Web Server (Ubuntu 24.04 – Predator Server)

<p align="center">
  <img src="https://github.com/Raja-Ramees.png" width="120">
</p>

<h2 align="center">Raja Ramees</h2>

<p align="center">
  <a href="https://www.linkedin.com/in/raja-ramees-804a7b262">
    <img src="https://img.shields.io/badge/LinkedIn-Raja%20Ramees-blue?style=for-the-badge&logo=linkedin">
  </a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/OS-Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white">
  <img src="https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker&logoColor=white">
</p>
## 🌍 Connect With Me

<p align="center">
  <a href="https://www.linkedin.com/in/raja-ramees-804a7b262">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-blue?style=for-the-badge&logo=linkedin">
  </a>
  <a href="mailto:yourmail@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact-red?style=for-the-badge&logo=gmail">
  </a>
</p>

> Predator Aurora is a **high-performance web service** running on Ubuntu 24.04 using **Nginx** as a reverse proxy.  
> This README provides a complete **installation, configuration, and usage guide** with visuals, tips, and best practices.

---
## 🛠️ Tech Stack

<p align="center">
  <img src="https://img.shields.io/badge/Linux-Expert-FCC624?style=for-the-badge&logo=linux&logoColor=black">
  <img src="https://img.shields.io/badge/Docker-Advanced-2496ED?style=for-the-badge&logo=docker&logoColor=white">
  <img src="https://img.shields.io/badge/Kubernetes-Hands--On-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white">
  <img src="https://img.shields.io/badge/AWS-Solutions%20Architect-FF9900?style=for-the-badge&logo=amazonaws&logoColor=black">
</p>

## 🔗 About the Author
- ## 🏆 Certifications

- ✅ AWS Solutions Architect  
- ✅ CompTIA Linux+  
- ✅ DevOps Certified  
- ✅ Docker & Kubernetes
<p align="center">
  <img src="https://raw.githubusercontent.com/docker/docs/main/static/img/docker-logo-white.png" width="420" />
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/raja-ramees-804a7b262" target="_blank">
    <img src="https://img.shields.io/badge/LinkedIn-Raja%20Ramees-0A66C2?logo=linkedin&logoColor=white&style=for-the-badge" />
  </a>
</p>

<h1 align="center"> INSTALLATION · Nginx Webserver · UBUNTU</h1>

<p align="center">
  <b>⚡ One Guide · One Flow · Zero Confusion ⚡</b><br/>
  <i>Built for beginners, trusted by professionals</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Ubuntu-22.04%20%7C%2024.04-FF6C37?logo=ubuntu&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Docker-Desktop-2496ED?logo=docker&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Setup-Type%20%7C%20GUI%20+%20CLI-0db7ed?style=for-the-badge" />
</p>

<hr/>

<p align="center">
  <img src="https://www.vectorlogo.zone/logos/docker/docker-ar21.svg" width="300" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Ubuntu-22.04%20%7C%2024.04-orange?logo=ubuntu&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Docker-Desktop-blue?logo=docker&style=for-the-badge" />
  <img src="https://img.shields.io/badge/Level-Beginner%20Friendly-green?style=for-the-badge" />
</p>

---

![Raja Ramees](www.linkedin.com/in/raja-ramees-804a7b262)

**Raja Ramees**  
- 🔗 [LinkedIn](https://www.linkedin.com/in/raja-ramees-804a7b262/)  
- 🌐 [Company Website](https://readyairesources.com/)  

---

## 🖥️ System Requirements

- Ubuntu 24.04 LTS (Server or Desktop)  
- Root or sudo privileges  
- Nginx installed  
- Predator Aurora project files
  ![Aurora AI Architecture](https://raw.githubusercontent.com/Raja-Ramees/Predator-Aurora-Web-Server-Setup-Nginx/0d1854e0ffa0ab71fc9546f32244139e8e4dacd3/Screenshot%202026-02-08%20100643.png)
  ![Architecture Screenshot](https://raw.githubusercontent.com/Raja-Ramees/Predator-Aurora-Web-Server-Setup-Nginx/main/Screenshot%202026-02-08%20101449.png)
![Ubuntu Logo](https://assets.ubuntu.com/v1/29985a98-ubuntu-logo32.png)  
![Nginx Logo](https://upload.wikimedia.org/wikipedia/commons/c/c5/Nginx_logo.svg)  
![Docker Logo](https://upload.wikimedia.org/wikipedia/commons/4/4e/Docker_%28container_engine%29_logo.png)

---

## 1️⃣ Install & Enable Nginx

💡 **Tip:** Always update packages before installation.

```bash
# Update system packages
sudo apt update

# Install Nginx
sudo apt install nginx -y

# Enable Nginx to start on boot
sudo systemctl enable nginx

# Start Nginx service
sudo systemctl start nginx

# Check Nginx status
systemctl status nginx.service
✅ Expected output: Active: active (running)

2️⃣ Configure Nginx for Predator Aurora

1️⃣ Create a site configuration:

sudo nano /etc/nginx/sites-available/predator


2️⃣ Example configuration:

server {
    listen 80;
    server_name _;

    root /home/raja/predator/wgdashboard;
    index index.html index.htm;

    location / {
        try_files $uri $uri/ =404;
    }
}


3️⃣ Enable site & remove default:

sudo ln -s /etc/nginx/sites-available/predator /etc/nginx/sites-enabled/
sudo rm -f /etc/nginx/sites-enabled/default


4️⃣ Test configuration & reload:

sudo nginx -t
sudo systemctl reload nginx

3️⃣ Test Predator Aurora
curl http://127.0.0.1


Expected response:

{"status":"Predator Aurora running"}



Example terminal output

4️⃣ Nginx Service Management
Command	Description
sudo systemctl restart nginx	Restart Nginx
sudo systemctl stop nginx	Stop Nginx
systemctl status nginx.service	Check status

💡 Tip: Use sudo journalctl -u nginx -f to follow live logs.

5️⃣ How Predator Aurora Works

Nginx acts as a reverse proxy for the project directory.

Requests to http://127.0.0.1 or server IP route to /home/raja/predator/wgdashboard.

Predator Aurora responds with JSON status or dashboard content.

Systemd ensures Nginx is always running and starts on boot.


Example dashboard view of Predator Aurora

6️⃣ Directory Structure Example
/home/raja/predator/wgdashboard/
│
├── index.html
├── app.js
├── styles/
└── scripts/

7️⃣ Optional: Docker Integration

If you want to run additional services like Open Web UI:

docker run -d -p 11437:8080 \
  --add-host=host.docker.internal:host-gateway \
  -v open-webui:/app/backend/data \
  --name open-webui \
  --restart always \
  ghcr.io/open-webui/open-webui:main


Access via browser: http://YOUR_SERVER_IP:11437

💡 Tip: Make sure your firewall allows port 11437.

8️⃣ Notes & Best Practices

✅ Always test Nginx config before reloading (nginx -t)

✅ Use curl to check backend API responses

⚠️ Ensure firewall allows port 80 for HTTP and 443 for HTTPS if needed

⚡ Place screenshots in your repo for visual references

💾 Keep your configuration in /etc/nginx/sites-available/ and enable via symbolic links

9️⃣ References

Nginx Official Docs

Ubuntu Nginx Guide

Made with ❤️ by Raja Ramees
LinkedIn
 | Company

---


---
