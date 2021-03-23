# nfs
nfs on Linux

## NFS端口
https://blog.csdn.net/fhqsse220/article/details/45668057  
```  
firewall-cmd --zone=public --permanent --add-port=2049/tcp
firewall-cmd --zone=public --permanent --add-port=111/tcp
firewall-cmd --zone=public --permanent --add-port=111/udp
firewall-cmd --zone=public --permanent --add-port=4046/udp
firewall-cmd --reload
```  


## NFS操作
https://blog.csdn.net/qq_36698956/article/details/81638843  

