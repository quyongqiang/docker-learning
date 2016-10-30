

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
docker inspect redis | grep -i networkse -A 15
```
