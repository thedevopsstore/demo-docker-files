from centos:7

## install apache
RUN yum install httpd -y

## expose the port on the container
EXPOSE 8080

## execute the start command for apche in the foreground
#CMD tail -f /dev/null
CMD ["/bin/bash", "/usr/sbin/apachectl", "-DFOREGROUND"]

