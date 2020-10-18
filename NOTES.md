注意事项

+ 主机hostname不能有下划线
+ docker使用中国镜像,helm使国内源
+ 虚拟机内在至少2G
+ 安装rancher命令行工具

> https://mp.weixin.qq.com/s?__biz=MzIyMTUwMDMyOQ==&mid=100010229&idx=1&sn=7fd8dd518b5899fe9331544e9c6ec0e5&chksm=68396e335f4ee7258e524e92cd7c42e3a9cabeab8d92d9ac148e56cc8f037c90a27c614c8f9e&xtrack=1&scene=0&subscene=10000&clicktime=1602104497&enterid=1602104497&ascene=7&devicetype=android-28&version=3.0.31.2308&nettype=WIFI&abtest_cookie=AAACAA%3D%3D&lang=zh_CN&exportkey=A7Wmb3MSV8vef3saDgmTDM8%3D&pass_ticket=U4YLEPG6gsOORch6YcfBgW0tNeUl5LY5FAXa2sTJ24r1uoqUsRLi3w3%2Fd1dByUvi&wx_header=1&platform=mac

>      docker run -itd -p 80:80 -p 443:443 \
        --restart=unless-stopped \
        -e CATTLE_AGENT_IMAGE="registry.cn-hangzhou.aliyuncs.com/rancher/rancher-agent:v2.4.2" \
        registry.cn-hangzhou.aliyuncs.com/rancher/rancher:v2.4.2



> 服务器初始化设置
> https://www.cnbugs.com/post-3190.html

# install k3s

#3 change yum source to ali 

> yum install wget
> mv /etc/yum.repos.d/CentOS-Base.repo /etc/yum.repos.d/CentOS-Base.repo.backup
> wget -O /etc/yum.repos.d/CentOS-Base.repo https://mirrors.aliyun.com/repo/Centos-7.repo
> yum makecache


## install k3s

> curl -sfL https://get.k3s.io | sh -
> curl -sfL http://rancher-mirror.cnrancher.com/k3s/k3s-install.sh | INSTALL_K3S_MIRROR=cn sh - 

