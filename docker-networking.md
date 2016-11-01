

#### 1.Create Network 
```
docker network create app
docker network inspect app
```
#### 2. Start Web Service (sinatra), and use network 'app'.
```
docker run -d -p 4567 --net=app --name webapp -v $PWD:/opt/webapp netqyq/sinatra
traceroute google.com
```
#### 3. Start DB Service(redis), and use network 'app'.
```
docker run -d --net=app --name db netqyq/redis
redis-cli  -h 172.18.0.2 -p 6379
```
#### 4. Testing DB Access(Write and write)
```
# write json data to redis, use post
curl -i -H 'Accept: application/json' -d 'name=Foo&status=Bar'  http://localhost:32776/json
# read the data from redis, use get
curl -i http://localhost:32776/json
```

#### 5 Source Code and Images

https://github.com/netqyq/dockerbook-code/tree/master/code/5/sinatra
hub.docker.com/netqyq


