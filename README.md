# centosmisc
centosmisc



RHEL/CentOS/Fedora使用yum update更新时，默认会升级内核。但有些服务器硬件（特别是组装的机器）在升级内核后，新的内核可能会认不出某些硬件，要重新安装驱动，很麻烦。所以在生产环境中不要轻易的升级内核，除非你确定升级内核后不会出现麻烦的问题。  

如果不想升级内核而只更新其他软件包，有两种方法：  

    1、修改yum的配置文件 vim /etc/yum.conf，在[main]的最后添加exclude=kernel*  
    2、直接在yum的命令后面加上如下的参数：  
    yum --exclude=kernel* update   
