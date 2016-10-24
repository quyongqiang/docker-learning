

*查看容器状态 *
```
docker inspect hello-world-nginx
docker inspect hello-world-nginx | grep -i  state -B 3 -A 3
docker inspect --format='{{ .State.Running }}' hello-world-nginx
```

