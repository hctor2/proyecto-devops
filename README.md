# Proyecto Final - Sistemas Operativos II

## Infraestructura DevOps en la Nube

Este proyecto demuestra una implementación básica de una infraestructura DevOps utilizando servicios en la nube, contenedores, orquestación y despliegue continuo.

## Tecnologías utilizadas

- AWS EC2
- Ubuntu Server
- Docker
- Docker Swarm
- Nginx
- GitHub
- GitHub Actions
- Security Groups

## Arquitectura general

Usuario → Internet → IP pública AWS → Security Group → EC2 Ubuntu → Docker Swarm → Nginx Web App

## Servicios desplegados

- Aplicación web en contenedor Docker
- Servicio web con Nginx
- Orquestación mediante Docker Swarm
- Dos réplicas del servicio web

## Comandos principales utilizados

```bash
docker build -t proyecto-devops-web .
docker swarm init
docker stack deploy -c docker-compose.yml devops
docker service ls
docker ps

```

## Seguridad básica

Se configuró un Security Group en AWS permitiendo únicamente los puertos necesarios para la demostración:

- Puerto 22 para conexión SSH
- Puerto 80 para acceso HTTP a la aplicación

En un entorno productivo, el acceso SSH debería limitarse únicamente a la IP del administrador.

## Evidencia

La aplicación se encuentra desplegada en una instancia EC2 de AWS y puede accederse mediante la IP pública del servidor.
