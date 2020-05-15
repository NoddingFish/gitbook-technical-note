# 配置Supervisor

> 参考：[Supervisor使用详解](https://www.jianshu.com/p/0b9054b33db3)

#### 说明：

​	配置文件：`/etc/supervisord.conf`

​	守护进程目录：`/etc/supervisord.d`

​	启动脚本：`/etc/init.d/supervisord`

​	

启动 Supervisor 

```shell
supervisord -c /etc/supervisord.conf
```

注意：

若执行命令 `supervisord -c /etc/supervisord.conf` 有误

执行：
`supervisorctl?stop?all` 停止所有进程
1、find / -name supervisor.sock
2、unlink /tmp/supervisor.sock 
3、ps -ef | grep supervisord
4、 kill -9 30027 //kill进程 
5、supervisord -c /etc/supervisord.conf