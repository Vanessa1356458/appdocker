Automatización de despliegue de una aplicación contenerizada utilizando Docker y GitHub Actions

Grupo #2 - Integrantes

- Ángel José Rosa Guifarro - 120350016
- Brayan Jesús Bustillo Elvir - 122310061
- Carmen Maribel Melgar Mejía - 107290127
- Christian Saul Calix Pineda - 121450021
- Cynthia Vanessa Rodríguez Silva - 120450041
- José Alonzo Ortega Serrano - 121280016
- Osman Adonay Mateo López - 121250002
- Selvin Alonso Miranda Martínez - 122250055


# Descripción del proyecto

Este proyecto implementa un flujo de integración continua y despliegue automatizado utilizando herramientas DevOps como Git, GitHub, Docker, GitHub Actions y Docker Hub.

La aplicación consiste en un programa desarrollado en Python que es empaquetado dentro de un contenedor Docker. Mediante un flujo automatizado, cada cambio realizado en el repositorio genera una nueva construcción de la imagen Docker y posteriormente la publica en Docker Hub.

El objetivo principal es demostrar el proceso completo desde la administración del código fuente hasta la distribución y ejecución de una aplicación contenerizada.


# Tecnologías utilizadas

- Python 3.11
- Git
- GitHub
- Docker
- Docker Hub
- GitHub Actions


# Estructura del proyecto
appdocker/
│
├── app.py
├── Dockerfile
├── README.md
│
└── .github/
└── workflows/
└── main.yml


# Descripción de archivos

1. app.py

Archivo principal de la aplicación desarrollado en Python.


2. Dockerfile

Archivo utilizado para definir la construcción de la imagen Docker. Utiliza una imagen base de Python 3.11, copia la aplicación dentro del contenedor y establece el comando que será ejecutado al iniciar.


3. main.yml

Archivo de configuración de GitHub Actions encargado de automatizar la construcción y publicación de la imagen Docker.



# Requisitos previos

Antes de ejecutar el proyecto es necesario tener instalado:

- Docker Desktop
- Git
- Cuenta de GitHub
- Cuenta de Docker Hub


# Instalación

1. Clonar el repositorio:

```bash
git clone https://github.com/USUARIO/appdocker.git


2. Ingresar al directorio: 

cd appdocker


3. Construcción manual de la imagen Docker

docker build -t usuario/appdocker:latest .


4. Ejecución de la aplicación

docker run usuario/appdocker:latest

Resultado esperado: Hola desde Docker


5. Integración Continua con GitHub Actions

El proyecto utiliza GitHub Actions para automatizar la construcción y publicación de imágenes Docker.

El flujo funciona de la siguiente manera:

Se realiza un cambio en el repositorio.
Se ejecuta un commit y push hacia la rama main.
GitHub Actions inicia automáticamente el workflow.
Se construye una nueva imagen Docker.
La imagen es publicada en Docker Hub.


6. Docker Hub

Imagen publicada: usuario/appdocker:latest

Para descargar la imagen: docker pull usuario/appdocker:latest


7. Ejecución desde otro equipo

Después de descargar la imagen: docker run usuario/appdocker:latest
