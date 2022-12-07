## Microsserviço Keycloak Auth

### Iniciando Keycloak.
cd composer
"docker-compose up -d" ou caso de alterações aplique "docker-compose up -d --build"


### Iniciando Projeto Go
cd goclient
go mod init goclient
go mod tidy
go run main.go

Start: http://localhost:8081/


## Endpoint Keycloak
http://localhost:8080/