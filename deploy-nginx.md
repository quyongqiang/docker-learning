#### Deploy Nginx
```
docker run -p  8080:80 -d nginx
docker ps -a
curl -i localhost:8080
# go into container 8a4(Container ID)
docker exec -it 8a4 /bin/bash

```

#### How to change static file and config file in nginx ?
```
# install vim
apt-get update
apt-get install -y vim

# config files
/etc/nginx/

# html files
/usr/share/nginx/html/
```
