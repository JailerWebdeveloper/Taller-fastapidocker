# FastAPI Docker

Este proyecto demuestra cómo crear y desplegar una aplicación FastAPI utilizando Docker.

## 📌 Requisitos
- Tener **Docker** instalado ([Descargar Docker](https://www.docker.com/get-started)).
- Tener una cuenta en [Docker Hub](https://hub.docker.com/).

## 🚀 Instalación y Uso

### 1️⃣ Clonar el Repositorio
```bash
git clone https://github.com/jailervega/Taller-fastapidocker.git
cd Taller-fastapidocker
```

### 2️⃣ Construir la Imagen Docker
```bash
docker build -t jailervega/fastapi-docker .
```

### 3️⃣ Ejecutar el Contenedor
```bash
docker run -d -p 8000:8000 jailervega/fastapi-docker
```

### 4️⃣ Verificar la Aplicación
Abre en el navegador:
- [http://localhost:8000](http://localhost:8000)

O prueba con `curl`:
```bash
curl http://localhost:8000
```

Deberías obtener la respuesta JSON:
```json
{"message": "Hello World"}
```

## 📤 Publicación en Docker Hub

### 5️⃣ Iniciar sesión en Docker Hub
```bash
docker login -u jailervega
```

### 6️⃣ Etiquetar la Imagen
```bash
docker tag fastapi-docker jailervega/fastapi-docker:v1
```

### 7️⃣ Subir la Imagen a Docker Hub
```bash
docker push jailervega/fastapi-docker:v1
```

## 🛠 Comandos Útiles
- Ver los contenedores en ejecución:
  ```bash
  docker ps
  ```
- Detener un contenedor:
  ```bash
  docker stop <CONTAINER_ID>
  ```
- Eliminar un contenedor:
  ```bash
  docker rm <CONTAINER_ID>
  ```
- Eliminar una imagen Docker:
  ```bash
  docker rmi jailervega/fastapi-docker:v1
  ```
- Limpiar contenedores detenidos:
  ```bash
  docker container prune
  ```

## 📎 Repositorio
[GitHub](https://github.com/JailerWebdeveloper/Taller-fastapidocker)
