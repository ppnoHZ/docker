# 常用命令
* docker pull [imagename] 下载镜像
* docker run [imagename]
    >--name 设置容器的名称，在对容器操作的时候就可以使用名称，如：--name mysqlwp

    > -e 设置容器的环境变量，如：-e MYSQL_ROOT_PASSWORD=wordpressdocker

    >-d 设置容器后台运行

    >-p 设置容器和host的端口映射，如：-p 80：80

    >--link 将两个容器关联起来，如：--link [容器名]:[镜像名]

# 容器操作

* docker rm 删除容器
    > -v 删除容器和存储
* docker stop $(docker ps -q)

* 批量操作可以使用$(docker ps -aq)

* docker ps 查看正在运行的容器
* docker ps -a 查看所有的容器



* docker build -t wordpress/test . 
  >从dockerfile中构建镜像