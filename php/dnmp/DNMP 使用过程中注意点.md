# DNMP 使用过程中注意点

1. #### `MySQL` 和 `Redis` 连接问题：

   ```
   # MySQL 项目中：
   mysql root 123456 # 服务器地址 用户名 密码
   
   # MySQL Navicat连接：
   localhost root 123456 # 服务器地址 用户名 密码
       
   # Redis 项目中：
   redis root  # 服务器地址 用户名 密码为空
   
   # Redis Medis连接：
   127.27.0.1 root  # 服务器地址 用户名 密码为空
   ```

   

2. #### 进入容器中：

   在 `windows` 中输入命令需要加 `winpty`

   ```bash
   $ winpty docker exec -it dnmp_mysql_1 bash
   ```

   

3. #### 命令：

   ```shell
   $ docker-compose up { -d } # 启动命令 [-d] 后台启动
   $ docker-compose down # 关闭
   $ docker-compose restart # 重启
   ```