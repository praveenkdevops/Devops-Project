# docker-Java-kubernetes-project
Deploying Java Applications with Docker and Kubernetes

Create Kubernetes Cluster:- https://nvtienanh.info/blog/cai-dat-kubernetes-cluster-tren-ubuntu-server-22-04

![image](https://github.com/praveenkdevops/docker-Java-kubernetes-project/assets/22557736/d986c164-9ad9-4ced-919c-823b398649a7)


Clone This repos on Kube-master and install Maven and Java...

cd docker-Java-kubernetes-project

cd shopfront/

mvn clean install

docker build -t praveenkumar1202/shopfront .

docker login

docker push praveenkumar1202/shopfront

cd ..

cd productcatalogue

mvn clean install

docker build -t praveenkumar1202/productcatalouge .

docker push praveenkumar1202/productcatalouge

cd ..

cd stockmanager/

mvn clean install

docker build -t praveenkumar1202/stockmanager .

docker push praveenkumar1202/stockmanager

![image](https://github.com/praveenkdevops/docker-Java-kubernetes-project/assets/22557736/9ee58b06-6f54-4c5e-9ed3-cedf36e761d0)

![image](https://github.com/praveenkdevops/docker-Java-kubernetes-project/assets/22557736/6c7b7354-0b5d-4e8f-95cd-24a8d5dbd304)

cd docker-Java-kubernetes-project/kubernetes

kubectl apply -f productcatalogue-service.yaml

kubectl apply -f  shopfront-service.yaml

kubectl apply -f  stockmanager-service.yaml

![image](https://github.com/praveenkdevops/docker-Java-kubernetes-project/assets/22557736/b72ae204-9517-41c6-8d34-798c00d23203)

Final Output 

![image](https://github.com/praveenkdevops/docker-Java-kubernetes-project/assets/22557736/52668e78-95c0-4dc9-9244-176b395cd63e)



