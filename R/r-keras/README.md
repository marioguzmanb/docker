# Jupyter Lab con R, Python y Keras (kaggle/rstats)

Este servicio utiliza la imagen `kaggle/rstats` para ofrecer un entorno de Jupyter Lab con soporte para R, Python y Keras, ideal para ciencia de datos y machine learning.

## Uso recomendado

Utiliza el archivo `docker-compose.yml` ubicado en **esta carpeta** (`r-keras/`) para levantar este servicio. Ejecuta los siguientes comandos desde aquí:

```bash
# Levanta el servicio en segundo plano
docker-compose up -d

# O detén el servicio
docker-compose down
```

Consulta el [README general](../README.md) para instrucciones completas de uso, volúmenes y personalización.

## Acceso manual (opcional)

Si prefieres ejecutar manualmente:

```bash
# Construye la imagen
docker build -t kaggle/rstats:1.0.0 .
# Ejecuta el contenedor
# (Ajusta la ruta de notebooks si lo deseas)
docker run -it -p 8086:8085 -v $(pwd)/../../notebooks/r-keras:/jovyan/work --name r-keras kaggle/rstats:1.0.0
```

Luego accede a [http://localhost:8086](http://localhost:8086) 

## Levantar el contenedor con docker-compose

La forma recomendada de iniciar este servicio es usando `docker-compose`. Desde la carpeta `docker/R/`, ejecuta:

