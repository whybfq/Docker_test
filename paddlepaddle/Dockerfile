
FROM paddlepaddle

#MATAINER is out of the time and label should be key=value
LABEL author=sanner    \
      test.version="0.0.1-beta"   \ 
      test.release-date="2018-01-10"   \
      test.version.is-production="false"

ENV PROJECT_DIR=/test
ENV PG_VERSION 9.3.4
#ENV APP_PORT=3000

ADD apt.tar.gz /etc/    #替换apt-get update的源，替换成为阿里云的，加速 (包中是目录)
WORKDIR $PROJECT_DIR
ADD . $PROJECT_DIR

#这里我们设置了每 5 秒检查一次（这里为了试验所以间隔非常短，实际应该相对较长），如果健康检查命令超过 3 秒没响应就视为失败，并且使用 curl -fs http://localhost/ || exit 1 作为健康检查命令。
#Here we set the inspected once every 5 seconds (here to test interval is very short, so actual should be relatively long), if the health check command more than 3 seconds without response as a failure, and use the curl - fs http://localhost/ | | exit 1 as a health check command.
HEALTHCHECK --interval=5s --timeout=3s  \
  CMD curl -fs http://localhost/ || exit 1 

#You can separate the data from containers and containers with volume.
VOLUME /home/test0   #to create a directory in host, the default shoule be at /var/lib/docker

RUN apt-get update && apt-get install -y \
    vim  \ 
    git  \
    tree  \ 
    inetutils-ping \
    && rm -rf /var/lib/apt/lists/*  
# added lines,it's producted by apt-get

RUN git clone https://github.com/PaddlePaddle/models/
#CMD ["python","$PROJECT_DIR/ecv_plate.py"] 

ENTRYPOINT [ "curl", "-s", "http://ip.cn" ]     #when you run the image with '-i' it will add it after CMD command while the CMD command can't
