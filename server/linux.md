# Linux指令相关
## golang相关

###  1.交叉编译

```shell
set GOARCH=amd64 &&  set GOOS=linux &&  go build -o main main.go
```



### docker相关

#### 1.批量删除 停止

```shell
docker stop $(docker ps -a | grep v1 | awk  '{print $1}')
docker rm $(docker ps -a | grep v1 | awk  '{print $1}')
docker rmi $(docker images|grep  "v1"| awk  '{print $3}')
```

