### 科学上网，搭建代理

####
SS

####
SSR

##### centos 6 x64
```bash
wget https://gist.githubusercontent.com/grasses/b1837aab1ce2149148d49dd458b483d1/raw/f9ebfc3a02fad9a00df9ab84c6d00369a0f7c778/XSSR.sh```q
```
```bash
chmod +x XSSR.sh && ./XSSR.sh
```
###### 更换2.6.32-504.3.3.el6.x86_64内核
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
###### 部署serverspeeder
```bash
wget -N --no-check-certificate https://github.com/91yun/serverspeeder/raw/master/serverspeeder.sh && bash serverspeeder.sh
```

##### centos 7 x64





