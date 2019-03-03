# Docker命令参数

* #### docker search 搜索镜像.
* #### docker login 登录docker.
* #### docker pull 下载镜像.
* #### docker images 查看已经存在的镜像.
* #### docker ps 查看容器状态.
* #### docker inspect获取容器/镜像的元数据.

#### inspect参数列表：

> ###### **-f :**指定返回值的模板文件。
>
> ###### **-s :**显示总的文件大小。
>
> ###### **--type :**为指定类型返回JSON。

* #### docker -event \(类似命令还有docker -logs\)参数列表：

> * **-f ：**根据条件过滤事件；
>
> * **--since ：**从指定的时间戳后显示所有事件;
>
> * **--until ：**流水时间显示到指定的时间为止；
>
> * --tail : 仅列出最近几条的日志信息.  
>   例子：docker -event -f "iamges"="hello-world" --since  "对应时间戳"/也可以直接使用时间.

* #### ![](/assets/import.png)-c参数代表所要执行的命令-------外加-d参数，可以使长期命令在后台执行，需要放在run后面，例如：docker run -d centos /bin/bash -c " command".返回的是长id，使用ps-a可以查看短id，短id是长id的前十二位.
* #### docker run --name &lt;name&gt;可以指定docker名，类似的命令还有docker create &lt;name&gt;创建一个容器但不启动他.
* #### docker stop &lt;容器名称/短ID&gt;来停止正在运行的容器，类似命令docker kill，docker kill -s 向容器放出警告.
* #### docker start &lt;容器名称...&gt;启动容器，类似命令docker restart.
* #### docker pause &lt;容器名称&gt;暂停容器0，类似命令还有unpause.
* #### docker rm &lt;容器名称&gt; 删除一个容器，docker rmi &lt;镜像名称&gt;删除镜像.
* #### docker rm -v $\(docker ps -aq -f status=exited\)删除所有已经退出的docker.
* #### docker attach &lt;容器id&gt;进入容器内部.
* #### docker exec -it &lt;短ID&gt; bash进入相关容器的bash，it参数代表以交互模式打开bash.
* #### ![](/assets/import1.png)
* #### docker export &lt;&gt;将文件系统写入到归档文件当中.例如：docker export -o mysql.'date +%Y%m%d'.tar &lt;容器名称&gt;.

## WEB

* #### 设置端口映射，docker run -d -p 80 httpd运行docker的web服务，修改端口使用docker run -d -p 80:80 http.
* #### docker -P代表以80端口启动docker.
* #### docker run -p 127.0.0.1:80:45163将容器的45162端口映射到本机的80端口.
* #### docker port &lt;容器名称&gt;查看端口映射情况.

## 容器rootfs命令

* #### docker commit 参数列表：

> * **-a :**提交的镜像作者
>
> * **-c :**使用Dockerfile指令来创建镜像；
>
> * **-m :**提交时的说明文字；
>
> * **-p :**在commit时，将容器暂停。

将容器a404c6c174a2 保存为新的镜像,并添加提交人信息和说明信息。

docker commit -a "" -m "" &lt;原镜像名称&gt;  &lt;新镜像名称&gt;.

























