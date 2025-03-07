1. build the app

docker run -it --name my_maven -v .:/usr/src/mymaven -w /usr/src/mymaven maven mvn clean install

2. build db01
docker build -t saleh1312/db01:v1.0 -f docker_files\Dockerfile.db01 .

3. build app01
docker build -t saleh1312/app01:v1.0 -f docker_files\Dockerfile.app01 .

3. build web01
docker build -t saleh1312/web01:v1.0 -f docker_files\Dockerfile.web01 .

3. build web01
docker build -t saleh1312/web01:v1.0 -f docker_files\Dockerfile.web01 .