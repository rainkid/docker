docker build -t "rainkide/nginx-php5" .
docker run -d -p 80:80 -v /home/www:/home/www -v /etc/nginx/sites-available:/etc/nginx/sites-available rainkide/nginx-php5
