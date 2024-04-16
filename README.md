# Kind

O kind é uma ferramenta para executar clusters locais do Kubernetes usando "nós" de contêineres Docker.
O kind foi concebido principalmente para testar o próprio Kubernetes, mas pode ser utilizado para desenvolvimento local ou CI.

# pré-requisitos

- [go 1.16+](https://go.dev)
- [docker](https://www.docker.com)

# Install

```bash
go install sigs.k8s.io/kind@v0.22.0
```

# Criar cluster

```bash
kind create cluster
```

```bash
kubectl cluster-info --context kind-kind
```

# pod.yaml

Para criar um unico pod use o `pod.yaml`

```bash
kubectl apply -f pod.yaml
```

# deployment.yaml

Para que os pods sejam recriados após cada atualização, use: 

```
kubectl apply -f deployment.yaml
```

# service.yaml

Para ocorrer um balanceamento entre os pods, use:

```
kubectl apply -f service.yaml
```

Para ter acesso aos pods use:

```bash
kubectl port-forward service/nginx-service 8080:80
```

# outros comandos

```
kubectl get pods
kubectl get nodes
kubectl get rs
kubectl delete <name>
```

```
kubectl delete pod <nome do pod>
```

# Link

[Iniciando com Kubernetes: Tutorial passo a passo](https://www.youtube.com/live/IeB9_PSGp6k?si=Xb1a4cC5QXx9hngk)