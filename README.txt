# Jenkins junto a Maven desplegado a traves de un Dockerfile para la compilacion y despliegue y entrega continua de una aplicacion java.
#Crear imagen
cd jenkinsdocker
docker build -t jenkins-cicd --no-cache
#Correr contenedor
docker run -d -p 8080:8080 -p 5000:5000 --name jenkins jenkins-cicd
