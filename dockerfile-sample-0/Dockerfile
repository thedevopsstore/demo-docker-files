FROM ubuntu 
RUN apt-get update 
RUN apt-get install apache2 -y
RUN apt-get install apache2-utils -y
RUN apt-get clean 
EXPOSE 80
WORKDIR /var/www/html/ 
COPY . .
CMD ["apache2ctl", "-D", "FOREGROUND"]

