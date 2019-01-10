FROM centos:7
MAINTAINER wubo 343618924@qq.com
ADD nginx-1.15.0.tar.gz /usr/local/wubo/
RUN yum install -y pcre* gcc* openssl* make
WORKDIR /usr/local/wubo/nginx-1.15.0
VOLUME /data
RUN ./configure --prefix=/usr/local/nginx --with-http_ssl_module --with-http_stub_status_module --with-pcre && make && make install
RUN echo "daemon off;" >> /usr/local/nginx/conf/nginx.conf
ENV PATH /usr/local/nginx/sbin:$PTAH
EXPOSE 80
CMD ["nginx"]