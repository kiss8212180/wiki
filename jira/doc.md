jira安装记录，如果是atlassian-jira-software-7.3.8-standalone.tar.gz包的话

1、解压后，参看README.txt

1、设置jira_home：

1）配置文件：atlassian-jira/WEB-INF/classes/jira-application.properties

jira.home =/opt/JIRA_HOM  #注意不要有空格，引号等，


2、启动
./bin/start-jira.sh 

3、默认是IP:8080 ，选择第二项 next：I will set it up  myself

   数据库选择了系统默认的数据库

4、修改默认端口
修改conf/server.xml中将8080改为80


5、备份恢复
备份：将JIRA_HOME整个目录备份
恢复：将备份文件整个覆盖即可

6、官网jira历史版本下载页面

http://www.atlassian.com/software/jira/download-archives


7、破解  
1)整除安装jira-7.3.6，此时试用期1个月  
2)安装成功后，关闭jira  
3)替换本目录下三个jar包到jira运行目录（atlassian-jira-software-7.3.6-standalone/atlassian-jira/WEB-INF/lib/），然后重启  
4)再查看jira服务器授权到期日 08/二月/33， 即：2033 2月 08日  
