# docker-mediawiki

## Add virtualhost to /etc/hosts
```bash
echo "127.0.0.1 mediawiki.localhost" >> /etc/hosts
```
```bash
git clone https://github.com/manzolo/docker-mediawiki.git
cd docker-mediawiki/
docker build -t manzolo/docker-mediawiki .
```
##Enter shell
```bash
docker run -it manzolo/docker-mediawiki /bin/bash
```
##Launch web server
```bash
docker run -d -p 8080:80 -p 33060:3306 manzolo/docker-mediawiki
```
##Navigate to
```
http://mediawiki.localhost:8080
```
##Navigate to phpmyadmin (user: "root" , empty password)
```
http://localhost:8080/phpmyadmin
```
