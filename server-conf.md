
#### install binarary files
#### setup env
```
PATH=$PATH:$HOME/bin:/data/docker
export DOCKER_HOST="unix:///data/docker/docker.sock"
```

#### start docker daemon
```
docker daemon -H unix:///data/docker/docker.sock &

```

#### test installation
```
docker info
```