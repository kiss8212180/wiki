运维知识纪要

1、阿里云机器尽量不要配置公网IP，可以走阿里云vpn ，或者vpc；slb  
2、mongo、redis尽量设置密码，大熊部门redis都是设置密码的  
3、nagios比较落伍了，zabbix监控，更先进的普罗米修斯（prometheus）  
4、ESXI虚拟化技术可靠性高，但是注意硬盘性能，是瓶颈，尤其是机器比较多的时候  
5、阿里云机ecs可以选择waf防护（不只是web防护，也可以防护主机），选择阿里安全服务  
6、阿里云机ecs硬盘并不可靠，注意备份；  
7、服务器只能买塔式服务器，没有机房  
8、阿里云机器开通自动快照，保障云盘数据的安全  
