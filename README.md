# AuthMS
El Auth MS es el microservicio que se encarga de realizar el registro y login de nuestros usuarios. También nos proporciona los tokens necesarios para poder autenticar nuestros endpoints.

## Dev

1. Clonar el repositorio
2. Instalar dependencias
3. Crear un archivo `.env` basado en el `.env.template`
4. Levantar el servidor de NATS
```
docker run -d --name nats-server -p 4222:4222 -p 8222:8222 nats
```
5. Tener levantados los microservicios que se van a consumor
6. Levantar el proyecto con `npm run start:dev`

## Nats
```
docker run -d --name nats-server -p 4222:4222 -p 8222:8222 nats
```

## PROD
Para desplegar en producción hay que generar la imagen ejecutando lo siguiente:
```
docker build -f Dockerfile.prod -t auth-ms-prod .
```