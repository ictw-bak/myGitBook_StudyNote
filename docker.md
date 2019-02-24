# Docker命令参数

* #### docker search 搜索镜像.
* #### docker login 登录docker.
* #### docker pull 下载镜像.
* #### docker ps 查看容器状态.
* #### ![](/assets/import.png)-c参数代表所要执行的命令-------外加-d参数，可以使长期命令在后台执行，需要放在run后面，例如：docker run -d centos /bin/bash -c " command".返回的是长id，使用ps-a可以查看短id，短id是长id的前十二位.
* #### docker run --name &lt;name&gt;可以指定docker名.
* #### docker stop &lt;容器名称/短ID&gt;来停止正在运行的容器，类似命令docker kill.
* #### docker start &lt;容器名称...&gt;启动容器，类似命令docker restart.
* #### docker pause &lt;容器名称&gt;暂停容器，类似命令还有unpause.
* #### docker attach &lt;容器id&gt;进入容器内部.
* #### docker exec -it &lt;短ID&gt; bash进入相关容器的bash，it参数代表以交互模式打开bash.
* #### ![](/assets/import1.png)
* 


