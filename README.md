# Lesson6

### This repository contains YAML manifest for deploying phpmyadmin and mysql services in kubernetes. Versions of images are fixed in mysql:8.0.30-debian for Mysql container and phpmyadmin:5.2.0 for PHPMyAdmin container.
##### You must have working kubernetes cluster for deployment. This YAML file was developped and tested with minikube version v1.26.0. Before executing commands, you have to copy file from this repository to your current folder.
##### Firstly you must enable ingress controller nginx with next command and wait for installation:
###### minikube addons enable ingress
##### Next step is deployment of whole virtual onix cluster for phpmyadmin appication. For deploying, use command:
###### kubectl apply -f lesson6.yaml
##### Now you can find an ip adress of your ingress-controller with next command:
###### kubectl get ingress -n onix
##### Add this ip adress to your file "hosts" and assign a domain name to this ip. Save the file.
##### Now you are able to check if your phpmyadmin application works properly. Insert assigned domain name in your browser and press enter.
