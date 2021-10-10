---
title: Linux Server Security
---

[00:02:12](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=132)

- update your software

[00:02:45](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=165)

- unintended package updates - install security stuff automaticaly

[00:03:23](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=203)

`sudo dpkg-reconfigure --priority=low unattended-upgrades`

[00:05:59](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=359)

docker containers - watchtower - automaticlaly update docker containers by redeploying them

[00:07:05](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=425)

ssh - strong password or public/private ssh keys

[00:07:18](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=438)

create separate user for running application

[00:10:13](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=613)

- passphrase for ssh keys - depend s on the security of a machine they are stored at

[00:12:25](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=745)

- disable password login and root login

[00:16:04](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=964)

-network security - expose services that you only need

[00:16:26](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=986)

`ss -ltpn` - show ports listened

[00:17:49](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=1069)

- enable firewall, e.g. ufw

[00:19:40](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=1180)

- open ports that you only need

[00:20:48](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=1248)

- ufw doesn't care about what runs in the container

[00:21:05](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=1265)

- it's like docker is ignored/whitelsited

[00:22:21](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=1341)

- use reverse proxy to use https in front of apps, that can't use it

[00:22:33](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=1353)

- nginx proxy manager - gui from nginx proxy

[00:23:22](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=1402)

- forbid internet acces to administrative interfaces

[00:24:07](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=1447)

- make separate network for administration, and connect to it directly or through vpn, dmz or other way

[00:25:10](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=1510)

- use IDS (intrusion detection system) or IPS (intrusion prevention system)

[00:25:19](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=1519)

- fail2ban

[00:28:09](https://www.youtube.com/watch?v=Bx_HkLVBz9M&t=1689)

- limit what applications can do on the system

[source](https://www.youtube.com/watch?v=Bx_HkLVBz9M)
