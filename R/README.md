# Jupyter Lab con R y Python (docker/R)

Este directorio contiene configuraciones para levantar entornos de Jupyter Lab con soporte para R y Python usando Docker. Hay dos variantes disponibles:

- **r-notebook**: Basado en la imagen oficial `jupyter/r-notebook`.
- **r-keras**: Basado en la imagen `kaggle/rstats` (incluye Keras y Python).

## Estructura
- `r-notebook/`  → Dockerfile y configuración para Jupyter Lab con R y Python
- `r-keras/`     → Dockerfile y configuración para Jupyter Lab con R, Python y Keras

## Uso rápido con docker-compose

1. Crea los directorios locales para tus notebooks (si no existen):

```bash
mkdir -p ./notebooks/r-notebook
mkdir -p ./notebooks/r-keras
```

2. Levanta ambos servicios o solo el que necesites:

```bash
docker-compose up -d
# o solo uno:
docker-compose up -d r-notebook
```

3. Accede a Jupyter Lab:
- r-notebook: [http://localhost:8085](http://localhost:8085)
- r-keras: [http://localhost:8086](http://localhost:8086)

4. Detén los servicios:

```bash
docker-compose down
```

## Personalización de volúmenes

Puedes editar el archivo `docker-compose.yml` para cambiar las rutas de los volúmenes y puertos según tus necesidades.

---

Para más detalles, revisa los README específicos en cada subcarpeta. 