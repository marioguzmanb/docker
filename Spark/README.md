# Configuración de ambiente de Spark
Se descarga la magen de [pyspark-notebook](https://hub.docker.com/r/jupyter/pyspark-notebook/), la que nos permite crear contenedores con todas las configuraciones necesarias para ejecutar código Pyspark en la versión 3.4.1 de Spark.

Para configurar esto se debe clonar el repositorio

```bash
git clone https://github.com/marioguzmanb/docker.git
```

Cambiarse de carpeta al servidor que queremos instalar SQL Server:

```bash
cd docker/Spark
```

Ejecutar el comando para la descarga de la imagen y configuración del contenedor:

```bash
docker-compose up
```

Una vez creado el contenedor y si se requiere levantar el contenedor existen dos maneras:
- Opción 1:
    
    ```bash
    docker-compose up
    ```

- Opción 2:
    
    ```bash
    docker start pyspark_container
    ```

Una vez levantado el contenedor y no se logra identificar el token para acceder al Jupyter notebook se requiere seguir los siguientes pasos:
- Entrar al contendor:
    ```bash
    winpty docker exec -it pyspark_container sh
    ```
- Ejecutar el comando para listar los servidores de Jupyter
    ```bash
    jupyter server list
    ```
- En la URL del navegador escribir:
    ```bash
    http://localhost:8888/lab
    ```
En caso de requerir el Token con el comando anterior se puede extraer. Si se requiere apagar el contenedor puedes detener Docker o bien ejecutar el comando para apagar solo el contenedor que contiene la aplicación de Spark.
```bash
docker stop pyspark_container
```