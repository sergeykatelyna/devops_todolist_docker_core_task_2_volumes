docker build -t mysql-local:1.0.0 -f Dockerfile.mysql .

docker run --name container-mysql-local -p 3306:3306 -d -v mysql-data:/var/lib/mysql mysql-local:1.0.0


docker build -t app-mysql:1.0.0 .

docker run --name container-app-mysql -p 8080:8080 -d app-mysql:1.0.0
