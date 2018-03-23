docker文档整理：

单机：

基础知识与概念参照 https://yeasy.gitbooks.io/docker_practice/ 

1.    运行一键安装脚本：
链接: https://pan.baidu.com/s/1c3HUeCwHegghI5HlXM4kHA 密码: stu5
（a 安装docker ; b 免sudo使用docker; c 配置了docker加速器；d 同时设置了私有仓库的地址）

http://blog.csdn.net/sannerlittle/article/details/76215053

2.  配置docker-machine:
 https://docs.docker.com/machine/install-machine/

3.  学习使用docker图形化的界面管理工具portainer官网
   a https://portainer.io/install.html  
   b https://portainer.readthedocs.io/en/stable/deployment.html#connect-to-a-swarm-cluster
   c 附：实时检测工具:  cadivisor
   d 常用的四种图形化管理工具:
https://juejin.im/post/596587a56fb9a06baa63d435

（补充：nvidia-docker安装   https://github.com/NVIDIA/nvidia-docker#quick-start  )

4. 学习Dockerfile编写：
  a https://store.docker.com/ (docker store)
  b.https://blog.fundebug.com/2017/05/15/write-excellent-dockerfile/

5.  使用docker-compose管理单机的多个容器（容器编排工具）：
   a. https://docs.docker.com/get-started/part3/#your-first-docker-composeyml-file
   b. https://www.jianshu.com/p/2217cfed29d7


查漏补缺：
Docker问答录100问： https://blog.lab99.org/post/docker-2016-07-14-faq.html



多机：
1.   docker swarm 
2.   service ( 相当于管理多机之间的多个容器)
https://docs.docker.com/get-started/part5/ 
3.  管理平台Mesos：

   a https://github.com/whybfq/Docker_test/blob/master/mesos/%E9%85%8D%E7%BD%AE%E5%91%BD%E4%BB%A4

b https://4hou.win/wordpress/?p=12098

c https://www.hi-linux.com/posts/8141.html

Marthon:
1.  https://mesosphere.github.io/marathon/docs/application-basics.html


扩展：

1. etcd学习:
a http://ralphbupt.github.io/2017/11/27/etcd%E5%AD%A6%E4%B9%A0%E7%AC%94%E8%AE%B0/

2. Kubernets:
(因为GFW的网络原因，在国内google的容器较难下载)
  a https://www.kubernetes.org.cn/doc-11
  b http://www.cnblogs.com/kevingrace/p/5575666.html



深入理解docker:

1. 自己动手写docker
https://github.com/xianlubird/mydocker

2.docker单主机容器网络 https://andyyoung01.github.io/2016/11/23/Docker%E7%9A%84%E5%8D%95%E4%B8%BB%E6%9C%BA%E5%AE%B9%E5%99%A8%E7%BD%91%E7%BB%9C/

3. docker跨主机容器网络
http://www.bocloud.com.cn/news/show-195.html

4.  docker源码
https://github.com/docker/docker.git 


常用：
1. docker image or container的导出与导入：
https://www.jianshu.com/p/8408e06b7273

2. docker 官网
https://docs.docker.com/

3. docker从入门到实践
https://yeasy.gitbooks.io/docker_practice/

4. 开放remote API(2375端口)：
  sudo vim /lib/systemd/system/docker.service
  修改 ExecStart=/usr/bin/dockerd -H fd:// -H tcp://0.0.0.0:2375  
  sudo systemctl daemon-reload 
  sudo systemctl restart docker.service
  netstat -an | grep 2377
