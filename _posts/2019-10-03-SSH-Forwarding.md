---
title: SSH Port Forwarding
published: true
---

# OpenSSH's SSH Port Forwarding Tech   

SSH를 통해서 Local / Remote 에 대한 포워딩으로 방화벽을 우회해서 접속하는 방법에 대한 설명.   

1. SSH Local Port Forwarding   
`ssh root@211.168.108.118 -N -L 5900:192.168.0.201:5900`

1. SSH Remote Port Forwarding

