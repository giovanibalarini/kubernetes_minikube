# kubernetes_minikube

No exemplo atual fiz utilizando Debian10

## Como instalar o minibuke

Possivelmente você vai querer subir uma maquina virtual em um virtualbox
da vida e instalar o minikube.

## Requisitos

* 2vCPU (minimo)
* 4GB RAM

## Instalando

#### Instalando as dependências e pacotes
```
# apt-get update && apt-get install sudo curl conntrack net-tools -y
```
#### Instalando o docker
```
# curl -fsSL https://get.docker.com | bash
# usermod -aG docker <seu usuario>
```
#### Instalando o minikube
```
# curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
# dpkg -i minikube_latest_amd64.deb
```

#### Configurando o minikube no host
```
# minikube start --vm-driver=none
```
![](https://i.imgur.com/piBmuaY.png)

#### Instalando kubectl, ferramenta de gerencia do cluster
```
# curl -LO https://storage.googleapis.com/kubernetes-release/release/`curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt`/bin/linux/amd64/kubectl && chmod u+x kubectl
```

![](https://i.imgur.com/MED9yMR.png)

**SUCESSO!!!**
## Fontes
[Instalando o minikube](https://minikube.sigs.k8s.io/docs/start/)

[Configurando minikube direto no host](https://minikube.sigs.k8s.io/docs/drivers/none/)

[Instalando kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)
