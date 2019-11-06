# 命令说明

## docker命令

1、Docker build 镜像，当前目录下的镜像文件Dockerfile
docker build -t runoob/ubuntu:15.10 .  
2、 docker image ls   #查看docker下镜像

## docker-compose命令

1、启动docker-compose应用  
docker-compose up  
2、docker-compose up -d  #detatch启动docker-compose  
3、docker-compose ps    #查看所有运行的进程  
4、 docker-compose run   命令  #启动一个一次性容器，执行完命令后删除容器  
5、docker-compose stop   #停止 -d 启动的容器（所有运行的容器)  
6、docker-compose down --volumes   #停止容器，删除volumes  

## docker-compose.yml配置文件说明

1. dockerfile args context说明

```yml
version: "3.7"
services:
  webapp:
    build:
      context: ./dir #指定需要build的内容，dockerfile或git地址或一个url所在的目录
      dockerfile: Dockerfile-alternate #指定替代的dockerfile文件，此时context也是必须指定的
      args: #指定在build时使用的参数，定义在docker-compose.yml下，这些参数最后是在dockefile中使用ARG关键字进行使用的，
        buildno: 1

```

