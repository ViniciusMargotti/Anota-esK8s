# Anotações-esK8s

https://phoenixnap.com/kb/install-minikube-on-ubuntu : Instalando minikube no Linux

## Minikube commands

 iniciando minikube
```bash 
minikube start 
``` 

```bash 
minikube service <POD> : Abrindo aplicação
``` 

abrindo dashboard do minikube
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







