FROM java:8
MAINTAINER wubo 343618924@qq.com
ADD zipkin.jar /usr/local/zipkin.jar
ENV  STORAGE_TYPE=elasticsearch ES_HOSTS=192.168.1.61:9200 RABBIT_ADDRESSES=192.168.1.61:5672
WORKDIR /usr/local/
CMD ["java","-jar","zipkin.jar"]
EXPOSE 9411
