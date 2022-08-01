# Lesson6

### This repository contains YAML manifests for deploying phpmyadmin and mysql services in kubernetes. Versions of images are fixed in mysql:8.0.30-debian for Mysql container and phpmyadmin:5.2.0 for PHPMyAdmin container.
##### You must have working kubernetes cluster for deployment. These YAML files were developped and tested with minikube version v1.26.0. Before executing commands, you have to copy files from this repository to your current folder.
##### Firstly you must enable ingress controller nginx with next command and wait for installation:
###### minikube addons enable ingress
##### Next step is creating your own namespace. For creating namespace, use command:
###### kubectl create -f create_onix_namespace.yaml
##### After creating namespace, next step is creating ingress with next command:
###### kubectl create -f ingress.yaml
##### Next step is deploying mysql. Mysql deployment, creating persistent volume and creating mysql network services are executing with next command:
###### kubectl create -f mysql.yaml
##### Next step is deploying phpmyadmin. Phpmyadmin deployment, creating phpmyadmin network services are executing with next command:
###### kubectl create -f phpmyadmin.yaml
##### Now you can find an ip adress of your ingress-controller with next command:
###### kubectl get ingress -n onix
##### Now you are able to check if your phpmyadmin application works properly. Insert described IP adress in our browser and press enter.
