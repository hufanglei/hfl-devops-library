
### 挂载
`docker run -d --name mysql03 -v mysql03_volume:/var/lib/mysql  -e MYSQL_ROOT_PASSWORD=jack123 mysql:5.7`

### 查看volume
` docker volume ls
`

### 查看某个volume
`docker volume inspect mysql03_volume`
