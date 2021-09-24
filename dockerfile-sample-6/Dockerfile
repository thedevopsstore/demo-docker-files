from centos:7

## install apache
RUN yum install httpd -y

## expose the port on the container
EXPOSE 8080

## Install AWS CLI in the container

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && unzip awscliv2.zip && sudo ./aws/install

## change the directory to apache document root


WORKDIR /var/www/html

## download an index.html from s3 bucket to copy it to /var/www/html/

RUN aws s3 cp s3://9am-weekend-jul/index.html .



## execute the start command for apche in the foreground
#CMD tail -f /dev/null
CMD ["/bin/bash", "/usr/sbin/apachectl", "-DFOREGROUND"]

