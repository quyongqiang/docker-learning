# 1.4 怎样下载墙外的镜像

## 使用Docker save/load 命令
```
# remote server
docker pull gcr.io/google_containers/pause:2.0
docker save -o gcr.io-google_containers-pause:2.0.tar gcr.io/google_containers/pause:2.0

# at local server, get this tar file, and load
docker load -i gcr.io-google_containers-pause:2.0.tar

```

## 使用私有镜像仓库

- [Docker开源轻量级镜像仓库](https://hub.docker.com/r/_/registry/)
- [Harbor开源企业级镜像仓库](https://github.com/vmware/harbor)


## 使用国内公有镜像仓库

- [灵雀云](https://hub.alauda.cn)
- [时速云](hub.tenxcloud.com)
- [daocloud加速器](https://www.daocloud.io/mirror.html)

## 使用代理服务器

- [企业级https开源代理服务器Squid](http://www.squid-cache.org)
- [轻量级https开源代理服务器TinyProxy](TinyProxy.github.io)

给docker配置代理
```
HTTP_PROXY
HTTPS_PROXY

```


## docker tag
