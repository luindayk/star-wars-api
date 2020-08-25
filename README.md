# star-wars-api

## Passos para rodar o app no cluster kubernetes

Subir o deployment:
```sh
kubectl apply -f star-wars-deployment.yaml
```
Subir o service:
```sh
kubectl apply -f star-wars-service.yaml
```
Criar o túnel para o app ficar acessível por conexão HTTP:
```sh
kubectl port-forward service/star-wars-api-service 9000:9000
```