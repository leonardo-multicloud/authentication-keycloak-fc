## Microsserviço Keycloak Auth

### Configuração necessária Ambiente.
-> Criar host DNS interno 127.0.0.1 kubernetes.docker.internal

## Build Docker goclient
docker build --progress=plain --no-cache -t api-autenticacao:staging .

## Iniciando ambiente
docker-compose.exe -f ..\composer\docker-compose.yml up -d

## Configuração Keycloak
Root URL http://kubernetes.docker.internal:8081
Valid redirect URIs: *

## Endpoint
http://kubernetes.docker.internal:8080/
http://kubernetes.docker.internal:8081/


### Iniciando Projeto Go [caso precise]
cd goclient
go mod init goclient
go mod tidy
go run main.go