---
title: PS1 Prompt & Rsync with NTFS
published: true
---   


# PS1 Bash Colorful Prompt    
`$ vi ~/.bash_profile`    

```rc
PS1="\[\e[36;1m\]\u@\[\e[31;1m\]\h \[\e[35;1m\]\w> \\$ \[\e[0m\]" 
export PS1
```   


# Rsync Windows File System     
```rc
yum install cifs-utils
mount -t cifs -o user="사용자명" //10.0.0.3/fileserver /mnt

rsync -avr --delete --exclude '/mnt/System Volume Information' /mnt /Data
``` 
## Rsync with BASH    
```rc  
#!/bin/bash
cd /
cp /dev/null /root/Mgmt/fileserver_sync.log
echo -e  "=========================================================\n" >> /root/Mgmt/fileserver_sync.log
date >> /root/Mgmt/fileserver_sync.log
rsync -avrh --delete --progress --exclude 'mnt/System Volume Information' /mnt /Data >> /root/Mgmt/fileserver_sync.log
date >> /root/Mgmt/fileserver_sync.log
echo -e "=========================================================\n" >> /root/Mgmt/fileserver_sync.log
```  






