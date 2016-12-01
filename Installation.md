
## 1. Install use binarary files, no systemctl scripts.
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

## 2. Install use yum on centos. Don't use default yum source, which is too old.

#### official
```
https://docs.docker.com/engine/installation
```

#### daocloud
```
http://get.daocloud.io/#install-docker

``
