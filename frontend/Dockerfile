#Dockerfile for cart frontend
#DockerCommand options
FROM index.docker.io/centos:7
RUN yum -y update
RUN yum -y install http php php-gd php-mysql
ADD code /var/www/html
ENV MY_DB_HOST_WRITE=test MY_DB_HOST_READ=test MY_DB_NAME=test MY_DB_USER=test MY_DB_PASS=test
#Command to run error logs on console
RUN  ln -sf  /proc/self/fd/1 /var/log/httpd/access_log
RUN ln -sf  /proc/self/fd/2 /var/log/httpd/errors_lo
CMD ["httpd", "-D", "FOREGROUND"]
