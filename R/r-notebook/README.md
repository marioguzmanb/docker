## Jupyter lab con Python y R
Esta imagen de Docker proviene desde dockerhub el proyecto [jupyter/r-notebook:r-4.2.2](https://hub.docker.com/layers/jupyter/r-notebook/r-4.2.2/images/sha256-4f134ddb729d65c3646ef7c8692d716da3d390e18c017ef0d4d237acfd784e44?context=explore) en el que podemos utilizar R y Python. En el cual tenemos dos caminos que podemos llegar a la misma solución

### Camino 1
Descargar la imagen desde dockerhub
```console
$docker pull jupyter/r-notebook:r-4.2.2
```
Levantar el contenedor
```console
$docker run -it -p 8888:8888 --name r-container jupyter/r-notebook:r-4.2.2
```
Ir al navegador y escribir en una nueva ventana **localhost:88888** y comenzar a desarrollar. Recordar que luego de terminar solo basta con levantar y baja el contenedor con los siguientes comandos
```console
# Levantar el conetenedor
$docker start r-container
# Bajar el contenedor (aunque este comando no es necesario, debido a que si bajas la aplicación se baja el contenedor de forma automática)
$docker stop r-container
```

### Camino 2
Construir la imagen, para este caso lo llamaremos rubuntu y el tag (version) 1.0.0
```console
$docker build -t rubuntu:1.0.0 .
```
Levantar el contenedor en el **Dockerfile** dejamos expuesto el puerto 8085, por lo tanto al momento de levantar el contenedor debemos definir que se levante con el puerto 8085
```console
$docker run -it -p 8085:8085 --name r-container rubuntu:1.0.0
```
Ir al navegador y escribir en una nueva ventana **localhost:8085** y comenzar a desarrollar. Recordar que luego de terminar solo basta con levantar y baja el contenedor con los siguientes comandos
```console
# Levantar el conetenedor
$docker start r-container
# Bajar el contenedor (aunque este comando no es necesario, debido a que si bajas la aplicación se baja el contenedor de forma automática)
$docker stop r-container
```
