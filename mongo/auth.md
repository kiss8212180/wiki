mongo设置账号密码：

1、修改/etc/mongo.conf  ,auth=true,如下

#数据库数据存放目录
dbpath=/datas/mongodb
#数据库日志存放目录
logpath=/datas/mongodb/logs/mongodb.log 
#以追加的方式记录日志
logappend = true
#端口号 默认为27017
port=27017 
#以后台方式运行进程
fork=true 
 #开启用户认证
auth=true
#关闭http接口，默认关闭http端口访问
#nohttpinterface=true
#mongodb所绑定的ip地址
#bind_ip = 127.0.0.1 
#启用日志文件，默认启用
journal=true 


2、重启mongo ，./mongod -f /etc/mongo.conf


3、登录mongo,初次登录，切换admin，并设置admin级别用户（root）账号密码
#mongo

>use admin  #切换到admin库下

>db.createUser({user:"root",pwd:"password",roles:["userAdminAnyDatabase"]})   #创建超级用户root和密码

> db.auth("root","password")    #登录认证

>show dbs    #认证通过，查看服务器下的所有库