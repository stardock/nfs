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

1. 服务端安装NFS  
`yum install nfs-utils rpcbind`  

2. 配置NFS服务端，编辑/etc/exports文件, 设置共享文件目录，如加入：
`/www/wwwroot 192.168.0.1(rw,sync,no_root_squash)`  

3. 先启动rpcbind服务,再启动NFS服务  

4. 当exports文件修改后，使用以下命令，不需要重启NFS服务，就可以重新挂载/etc/exports里面的设定  
`exportfs -arv`  
