# Automatización y DevOps con Docker

Este proyecto documenta el proceso de configuración de un flujo de trabajo CI/CD (Integración Continua y Despliegue Continuo) para una aplicación utilizando Git, GitHub, GitHub Actions y Docker.

## Descripción del Proyecto

El objetivo de este repositorio es automatizar la construcción y publicación de una aplicación contenerizada. Cada vez que se sube un cambio a la rama `main`, GitHub Actions construye automáticamente una imagen de Docker y la publica en Docker Hub, garantizando que el despliegue sea eficiente y estandarizado.

## Tecnologías Utilizadas

- **Git**: Sistema de control de versiones.
- **GitHub**: Plataforma de alojamiento de repositorios.
- **GitHub Actions**: Automatización de flujos de trabajo (CI/CD).
- **Docker**: Creación y gestión de contenedores.
- **Docker Hub**: Registro para alojar las imágenes de Docker.

## Flujo de Trabajo (CI/CD)

1. **Desarrollo**: El código fuente se gestiona mediante Git.
2. **Integración**: Los cambios se envían a GitHub.
3. **Automatización**: GitHub Actions detecta el cambio, construye la imagen Docker usando el `Dockerfile` y la envía (push) a Docker Hub.
4. **Despliegue**: La imagen está lista para ser descargada y ejecutada en cualquier entorno compatible.

## Configuración y Requisitos

Para replicar este entorno, se requiere:

- Sistema operativo Windows 10 u 11.
- Git instalado.
- Docker Desktop instalado y en ejecución.
- Cuenta en GitHub y Docker Hub.

### Variables de Entorno (Secrets)

Para que el flujo funcione, se deben configurar los siguientes *Secrets* en el repositorio de GitHub (`Settings` -> `Secrets and variables` -> `Actions`):

- `DOCKER_USER`: Tu nombre de usuario en Docker Hub.
- `DOCKER_PASS`: Un *Personal Access Token* (PAT) generado en Docker Hub con permisos de lectura y escritura.

## Cómo ejecutar la aplicación

Una vez publicada la imagen, puedes ejecutar la aplicación en cualquier máquina con Docker instalado mediante el siguiente comando:

```bash
docker run <tu-usuario-docker>/appdocker:latest

## 👩‍💻 Autora

*Vanessa Rodriguez*
