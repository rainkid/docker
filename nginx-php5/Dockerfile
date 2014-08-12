FROM rainkide/ubuntu

RUN apt-get update 
RUN apt-get -y install nginx 
RUN apt-get -y install php5-fpm php5-mysql php5-imagick php5-mcrypt  php5-gd

RUN echo "\ndaemon off;" >> /etc/nginx/nginx.conf

# Define mountable directories.
VOLUME ["/home/www", "/etc/nginx/sites-available", "/var/log/nginx"]

# Define working directory.
#WORKDIR /etc/init.d

# Define default command.
#CMD["nginx"]

EXPOSE 80
EXPOSE 443
EXPOSE 9000

CMD service php5-fpm start && nginx

