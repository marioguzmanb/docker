# Jupyter Lab con Python 3.8 (Docker)

Este entorno permite ejecutar Jupyter Lab con Python 3.8 usando Docker y Docker Compose. Incluye instalación automática de dependencias desde `requirements.txt` y persistencia de notebooks en un volumen local.

## Requisitos previos

- [Docker](https://docs.docker.com/get-docker/) instalado
- [Docker Compose](https://docs.docker.com/compose/install/) instalado

## Estructura de archivos

```
.
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
└── notebooks/           # (se crea automáticamente si no existe)
```

## Paso a paso

1. **Clona o navega a este directorio:**
   ```bash
   cd docker/python/py38
   ```

2. **(Opcional) Crea la carpeta para tus notebooks:**
   ```bash
   mkdir -p notebooks
   ```

3. **Agrega tus dependencias en `requirements.txt`**
   - Edita el archivo `requirements.txt` para incluir los paquetes de Python que necesitas.

4. **Construye y levanta el contenedor:**
   ```bash
   docker-compose up --build
   ```

5. **Accede a Jupyter Lab:**
   - Abre tu navegador en: [http://localhost:8888](http://localhost:8888)
   - El token de acceso aparecerá en la consola donde ejecutaste el comando.

6. **Guarda tus notebooks:**
   - Todos los archivos creados o modificados en Jupyter Lab se guardarán en la carpeta local `notebooks/`.

## Dependencias

- Python 3.8 (imagen base: `python:3.8-slim-buster`)
- Paquetes listados en `requirements.txt` (instalados automáticamente al construir la imagen)
- Jupyter Lab

## Comandos útiles

- **Detener el contenedor:**
  ```bash
  docker-compose down
  ```
- **Reconstruir después de cambiar `requirements.txt`:**
  ```bash
  docker-compose up --build
  ```