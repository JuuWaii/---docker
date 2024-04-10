```
# 新建文件夹 lx-music-sync-server 和 子目录
mkdir -p /volume2/docker/lx-music-sync-server/{data,logs}

# 进入 lx-music-sync-server 目录
cd /volume2/docker/lx-music-sync-server

# 运行容器
docker run -d \
   --restart unless-stopped \
   --name lx-music-sync-server \
   -p 9527:9527 \
   -v $(pwd)/data:/server/data \
   -v $(pwd)/logs://server/logs \
   -e LX_USER_user1=mypassword123 \
   wbsu2003/lx-music-sync-server


```

其中连接码默认为 mypassword123
---
原文链接：https://blog.csdn.net/wbsu2004/article/details/129871452