为什么我们需要挂载配置文件
因为为了压缩容器大小 一切不需要的软件都不会安装 包括vim

所以为了方便修改配置文件 我们使用挂载的方式
docker run --name nginx -p 80:80 -d nginx


另外 一定要注意 因为容器重启会丢失内部数据，因此要将需要持久化的文件挂载到宿主机中，以防数据丢失。
所以mysql数据库一定要挂载数据目录！！
之前就遇到过这个问题 strapi 容器重启后 数据库中的数据就丢失了
