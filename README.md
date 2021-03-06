# 科学上网，搭建代理

## 1. SS

### 1.1 centos 7 x64 

> #### * 部署SS
```bash
wget --no-check-certificate https://raw.githubusercontent.com/teddysun/shadowsocks_install/master/shadowsocks-libev.sh && chmod +x shadowsocks-libev.sh && ./shadowsocks-libev.sh 2>&1 | tee shadowsocks-libev.log
```
> #### * 卸载SS
```bash
./shadowsocks-libev.sh uninstall
```
> #### * 部署完成后可安装serverspeeder提速，方法见下文

****

## 2. SSR

### 2.1 centos 6 x64  

> #### * 更换2.6.32-504.3.3.el6.x86_64内核  
```bash
rpm -ivh http://soft.91yun.org/ISO/Linux/CentOS/kernel/kernel-firmware-2.6.32-504.3.3.el6.noarch.rpm
```
```bash
rpm -ivh http://soft.91yun.org/ISO/Linux/CentOS/kernel/kernel-2.6.32-504.3.3.el6.x86_64.rpm --force
```
```bash
rpm -qa | grep kernel
```
```bash
uname -r
```

> #### * 部署SSR
```bash
wget https://gist.githubusercontent.com/grasses/b1837aab1ce2149148d49dd458b483d1/raw/f9ebfc3a02fad9a00df9ab84c6d00369a0f7c778/XSSR.sh && chmod +x XSSR.sh && ./XSSR.sh
```

> #### * 部署serverspeeder
```bash
wget -N --no-check-certificate https://github.com/91yun/serverspeeder/raw/master/serverspeeder.sh && bash serverspeeder.sh
```

### 2.2 centos 7 x64  

> #### * 更换3.10.0-229.1.2.el7.x86_64内核  
```bash
rpm -ivh http://soft.91yun.org/ISO/Linux/CentOS/kernel/kernel-3.10.0-229.1.2.el7.x86_64.rpm --force
```
```bash
grub2-set-default 'CentOS Linux (3.10.0-229.1.2.el7.x86_64) 7 (Core)'
```
```bash
grub2-editenv list
```
```bash
rpm -qa | grep kernel 
```
```bash
uname -r
```

> #### * 配置 ifconfig  
```bash
yum install net-tools
```

> #### * 部署SSR
```bash
wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/ssr.sh && chmod +x ssr.sh && bash ssr.sh
```

> #### * 部署serverspeeder
```bash
wget -N --no-check-certificate https://github.com/91yun/serverspeeder/raw/master/serverspeeder.sh && bash serverspeeder.sh
```

****

## 3. V2ray

### 3.1 centos 7 x64 

> #### * 更换内核并部署serverspeeder方法同上

> #### * 配置 ifconfig  
```bash
yum install net-tools
```
> #### * 安装wget zip unzip
```bash
yum -y install wget zip unzip
```
> #### * 下载脚本
```bash
wget https://install.direct/go.sh
```
> #### * 安装V2ray
```bash
bash go.sh
```
> #### * 设置开机自启动
```bash
systemctl enable v2ray
```
> #### * 开启服务
```bash
systemctl start v2ray
```
> #### * 查看配置文件
```bash
cat /etc/v2ray/config.json
```
> #### * 查看防火墙状态
```bash
systemctl status firewalld
```
> #### * 永久关闭防火墙
```bash
systemctl disable firewalld
```
