# Anotações-K8s

https://phoenixnap.com/kb/install-minikube-on-ubuntu : Instalando minikube no Linux

https://docs.docker.com/engine/install/ubuntu/ : Instalando Docker no Linux

## Minikube commands

 Iniciando minikube
```bash 
minikube start 
``` 

Abrindo aplicação do POD
```bash 
minikube service <POD>
``` 

Abrindo dashboard do minikube
```bash   
minikube dashboard
``` 

## Docker commands

Salvar Imagem Docker local para deployment no MiniKube(K8s)
```bash   
docker save srlopes/fortunecookie:v1 | (eval $(minikube docker-env) && docker load) 
``` 

Visualizar imagens da maquina
```bash   
docker-images
``` 

## K8s commands

Criando deploy Spring/Minibube
```bash   
kubectl create deployment fortunecookie --image=srlopes/fortunecookie:v1  
``` 

Liberando acesso da porta 8080 para a aplicação
```bash   
kubectl expose deployment fortunecookie --type=LoadBalancer --port=8080   
``` 







