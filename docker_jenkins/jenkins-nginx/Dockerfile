FROM centos:centos7

RUN yum -y update; yum clean all
RUN yum -y install epel-release
RUN yum -y install nginx

RUN rm -f /etc/nginx/conf.d/*
#RUN rm /etc/nginx/conf.d/example_ssl.conf

COPY conf/jenkins.conf /etc/nginx/conf.d/jenkins.conf
COPY conf/nginx.conf /etc/nginx/nginx.conf

EXPOSE 80

CMD ["nginx"]
