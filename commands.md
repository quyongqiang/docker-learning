

查看容器状态
```
docker inspect hello-world-nginx
docker inspect hello-world-nginx | grep -i  state -B 3 -A 3
docker inspect --format='{{ .State.Running }}' hello-world-nginx
```

删除容器
```
docker rm -f container_id
docker rm container_id
```


删除image
```
docker rmi image_id
```

启动容器
```
docker run -d -p 8080:3000 nginx
```

连接到容器
```
docker exec -it container_id /bin/bash
```

停止所有容器
```
docker rm -f `docker ps -a -q`
```

查看redis容器的网络配置
```
docker inspect redis | grep -i networks -A 15
```
查看docker进程

```
# ps -ef | grep docker
root     20820     1  3 01:59 ?        00:00:00 /usr/bin/docker-current daemon --exec-opt native.cgroupdriver=systemd --selinux-enabled --log-driver=journald
```
刪除docker, centos
```
 yum remove  docker*
```
