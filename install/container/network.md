
- 在linux上，网络的隔离是通过network namespace来管理的，不同的network namespace是互相隔离的
ip netns list：查看当前机器上的network namespace
network namespace的管理

```shell
ip netns list #查看
ip netns add ns1 #添加
ip netns delete ns1 #删除
```

### 查看docker的网络列表
`docker network ls`

### 查看某个docker网络
`docker network inspect bridge` 【推荐】
<br/>
`docker inspect tomcat-net
`
## 创建一个网络
`docker network create tomcat-net
`

## 将一个容器加入到一个自定义的网络中
`docker network connect tomcat-net tomcat01
`

### 容器启动时指定 自定义的network网络
`docker run -d --name tomcat12 --network tomcat-net tomcat`

### 容器启动时 默认网络，可以用link指定【生产中很少用】
其中tomcat02使用的是默认docker0的网络，tomcat01是新建的网络。 
<br/>
`docker run -d --name tomcat01 --link tomcat02 tomcat`

