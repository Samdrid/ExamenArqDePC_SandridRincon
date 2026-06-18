# Examen Final - Arquitectura Orientada a Servicios

## Objetivo del proyecto
Diseñar, versionar, desplegar y eliminar una infraestructura en la nube (una instancia EC2 con un Security Group) utilizando AWS, AWS CloudFormation y GitHub Actions, aplicando buenas prácticas de control de versiones mediante Git Flow y trabajo colaborativo.

## Tecnologías utilizadas
- AWS (Amazon Web Services)
- AWS CloudFormation (Infraestructura como código)
- AWS EC2 (Amazon Linux)
- GitHub Actions (automatización de despliegue)
- Git / Git Flow (control de versiones y trabajo colaborativo)

## Funcionalidad de Deploy
El workflow `deploy.yml` se ejecuta al hacer push a `main` o manualmente desde Actions. Valida el template de CloudFormation, despliega el stack (creando la instancia EC2, el Security Group con puerto 80 habilitado, y la página web mediante UserData) y muestra la URL pública resultante.

## Funcionalidad de Destroy
El workflow `destroy.yml` se ejecuta manualmente desde Actions. Elimina el stack de CloudFormation completo, lo que borra automáticamente la instancia EC2 y el Security Group, evitando costos adicionales en AWS.

## Objetivo del template EC2 (`template/ec2.yaml`)
Define como código la infraestructura del examen: una instancia EC2 Amazon Linux, un Security Group con el puerto 80 (HTTP) habilitado, y un script de UserData que instala un servidor web y publica una página con los datos del estudiante.

## Autor
- **Nombre:** Yeilis Sandrid Nogoa Rincón
- **Código estudiantil:** 0192375