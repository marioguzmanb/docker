# Jupyter Lab con R y Python (jupyter/r-notebook)

Este servicio utiliza la imagen oficial `jupyter/r-notebook` para ofrecer un entorno de Jupyter Lab con soporte para R y Python.

## Uso recomendado

Utiliza el archivo `docker-compose.yml` ubicado en **esta carpeta** (`r-notebook/`) para levantar este servicio. Ejecuta los siguientes comandos desde aquí:

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
docker build -t rubuntu:1.0.0 .
# Ejecuta el contenedor
# (Ajusta la ruta de notebooks si lo deseas)
docker run -it -p 8085:8085 -v $(pwd)/r-notebook:/home/jovyan/work --name r-notebook rubuntu:1.0.0
```

Luego accede a [http://localhost:8085](http://localhost:8085)
