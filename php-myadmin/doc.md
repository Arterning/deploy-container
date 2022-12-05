telnet localhost 3306
ufw allow 3306
ufw delete allow 3306

关于容器使用需要注意一点
如果你的挂载了外部目录 在你重新启动容器的时候 可能还是使用的旧数据
比如你如果想要重新设置数据库密码 由于旧挂载目录的存在可能是失败的。
因为docker compose remove 删除容器并不会删除挂载目录
