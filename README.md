# ft_services

### 🎯 Object

The projects is about deploying automatically a cluster of microservices using homemade container images and an orchestration tool. The orchestration tool for managing the containers and their interconnections is kubernetes, it creates and maintains the cluster state for us. Each container image is build from scratch from the alpine linux base image for lightweight and learning purpose. The whole service we are going to run is made of the following microservices (each in its dedicated container).

Nginx server

FTPs server

Wordpress

PhpMyAdmin (for managing the wordpress database)

MySQL database (database for the wordpress site)

Grafana (visualisation for monitoring the containers)

INfluxDB database (database for the grafana)

From the outside world, the access to the cluster is made through a load balancer. MetalLB is used for this purpose. It will publish only one IP to access the whole cluster.

# SCHEMA OF OUR CLUSTER

![image](https://user-images.githubusercontent.com/52714837/130298299-09688fa4-28a2-41d1-8e98-93230f97ef7e.png)

### 💻 How to Run

```command
sh ./setup.sh
```
Kubernets dashboard

After you started setup.sh Automatically in 20 seconds you will be directed to the kubernetes dashboard page

it will display something like that but with all images

![image](https://user-images.githubusercontent.com/52714837/130298635-9740f3b6-8042-4067-ac39-4f7ae520d7d5.png)
