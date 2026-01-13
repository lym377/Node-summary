## Usage

```bash
curl -s https://raw.githubusercontent.com/vevc/one-node/refs/heads/main/webhostmost/install.sh |
env DOMAIN=example.com REMARKS=webhostmost-server3 bash
```

## Acknowledgements

- [@闹海金蛟](https://www.youtube.com/@%E9%97%B9%E6%B5%B7%E9%87%91%E8%9B%9F)
- [town95/node-ws](https://github.com/town95/node-ws)
- 
最安全的 webhostmost 代理节点，无惧管理员密码泄漏，无惧 UUID 泄漏，无需代码加密混淆，无需设置文件访问权限

webhostmost 注册地址：
https://webhostmost.com/free-web-hosting
项目介绍
1、安装脚本项目

https://github.com/vevc/one-node

    安装 nodejs-vless 代理
    安装 cron 定时任务：进程保活，清除僵尸进程，清理磁盘（/home/$USER/Maildir/*）

2、nodejs-vless 代理项目

https://github.com/vevc/nodejs-vless

    代理节点
    Web Shell

无惧 UUID 泄漏原理

修改了 VLESS 协议的鉴权逻辑
<img width="705" height="269" alt="截屏2026-01-13 11 10 07" src="https://github.com/user-attachments/assets/b69c223b-9b94-4590-8ae6-4bf3703a9813" />

相关链接：
VLESS 协议定义：https://xtls.github.io/development/protocols/vless.html

MD5 逆向
```
/123 > 4767df9bd528bea28492455ba17bb5fb

/9ROAYQtEF3WJPh > 1b9b4e6abec2d26c0f4a733a8f152c3a

echo -n '/123' | md5sum | awk '{print $1}'

https://cmd5.com

```




