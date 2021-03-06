# Anotações-esK8s
anotações referente ao estudo do K8S



## Abrir Endereço do projeto no Minikube (k8s)
minikube service fortunecookie


## Salvar Imagem Docker local para deployment no MiniKube(k8s)
docker save srlopes/fortunecookie:v1 | (eval $(minikube docker-env) && docker load)

