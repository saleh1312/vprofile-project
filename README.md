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

4. login to your docker hub

5. push images
docker push saleh1312/db01:v1.0 
docker push saleh1312/app01:v1.0
docker push saleh1312/web01:v1.0

6. run k8s cluster
cd k8s
vagrant up
vagrant ssh controlplane
cd /vagrant/vprof_files
kubectl apply -f .
kubectl get all
kubectl get nodes -owide
kubectl get svc