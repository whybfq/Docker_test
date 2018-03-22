docker文档整理：

单机：
基础知识与概念参照 https://yeasy.gitbooks.io/docker_practice/ 
1.    运行向成的一键安装脚本：
（a 安装docker ; b 免sudo使用docker; c 配置了docker加速器；d 同时设置了私有仓库的地址） http://blog.csdn.net/sannerlittle/article/details/76215053
2.  配置docker-machine:
 https://docs.docker.com/machine/install-machine/
3.  学习使用docker图形化的界面管理工具portainer官网
   https://portainer.io/install.html  
   https://portainer.readthedocs.io/en/stable/deployment.html#connect-to-a-swarm-cluster
 附：实时检测工具:  cadivisor

常用的四种图形化管理工具:
https://juejin.im/post/596587a56fb9a06baa63d435

（补充：nvidia-docker安装   https://github.com/NVIDIA/nvidia-docker#quick-start )

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

https://github.com/whybfq/Docker_test/blob/master/mesos/%E9%85%8D%E7%BD%AE%E5%91%BD%E4%BB%A4

https://4hou.win/wordpress/?p=12098

Marthon:
1.  https://mesosphere.github.io/marathon/docs/application-basics.html
