Claw cloud 容器 VPS 安装 Node.js 版本科学上网代理服务

Claw cloud 注册地址：
https://console.run.claw.cloud/signin?link=TSWVWVN3G294

容器 VPS 项目地址：
https://github.com/vevc/ubuntu

nodejs-vless 项目地址：
https://github.com/vevc/nodejs-vless
说明

有 xray, 不用 Node.js
安装

mkdir ~/nodejs-vless
cd ~/nodejs-vless
wget https://raw.githubusercontent.com/vevc/nodejs-vless/refs/heads/main/app.js
wget https://raw.githubusercontent.com/vevc/nodejs-vless/refs/heads/main/package.json
npm install
PORT=3000 UUID=10889da6-14ea-4cc8-97fa-6c0bc410f121 DOMAIN=example.com node app.js

使用 Supervisor 管理并启动

[program:nodejs-vless]
environment=PATH="/home/vevc/.nvm/versions/node/v20.19.4/bin:/usr/sbin:/usr/bin:/sbin:/bin",UUID="10889da6-14ea-4cc8-97fa-6c0bc410f121",DOMAIN="example.com"
directory=/home/vevc/nodejs-vless
command=node app.js
autostart=true
autorestart=true
user=vevc
