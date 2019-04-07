# Ubuntu下安装使用Redis

```
sudo apt-get update
sudo apt-get install redis-server
```

## 启动Redis

```
redis-server
```

## 查看Redis是否启动

```
redis-cli
```

## 出现以下则证明redis已成功启动

```
┬─[suofeiya@suofeiya-PC:~]─[19时11分00秒]
╰─>$ redis-cli
127.0.0.1:6379> ping
PONG
```

## 通过以下命令可以避免出现中文乱码

```
redis-cli --raw
```

## Redis 的配置文件在/etc/redis.conf，为Redis添加密码

```
requirepass yourpassword
```



