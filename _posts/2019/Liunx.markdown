---
layout: "post"
title: "Liunx"
date: "2019-05-23 14:57"
---

### 常用命令
1.  滚动查看`log.log`文件
    ```tail -f log.log```

2. 启动`jar`程序
    ```
    nohup java -Xms4096m -Xmx4096m -XX:PermSize=128m -XX:MaxPermSize=256m  -jar icp-core-1.0-SNAPSHOT.jar >log.log 2>&1 &
    ```

3. 查看进程`eg：java`
    ```ps -ef |grep java```

4. 查看`tcp`连接总数
    ```
    netstat -n| awk '/^tcp/ {++S[$NF]} END {for(a in S) print a, S[a]}'
    ```

5. 查看`tcp`连接状态详情
    ```netstat -an|more```

6. 查看连接总数
    ```ss -s```
