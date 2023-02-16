## Jupyter lab con Python y R
Esta imagen de Docker proviene desde dockerhub el proyecto [kaggle/rstats](https://hub.docker.com/layers/kaggle/rstats/latest/images/sha256-72f23c48fa19771e8ec009ac9175993249a855e466b7eb6baf9b5fb01c4b17fc?context=explore) en el que podemos utilizar R y Python. Esta imagen es similar o igual al ambiente que nos provee [kaggle](www.kaggle.com) para desarrollar.

### Levantar la aplicación
Construir la imagen, para este caso lo llamaremos kaggle/rstats y el tag (version) 1.0.0
```console
$docker build -t kaggle/rstats:1.0.0 .
```
Levantar el contenedor en el **Dockerfile** dejamos expuesto el puerto 8085, por lo tanto al momento de levantar el contenedor debemos definir que se levante con el puerto 8085
```console
$docker run -it -p 8085:8085 --name r-container kaggle/rstats:1.0.0
```
Ir al navegador y escribir en una nueva ventana **localhost:8085** y comenzar a desarrollar, sin embargo, es muy probable que les solicite un token el cual podemos capturar desde la consola dónde levantamos el contenedor. Recordar que luego de terminar solo basta con levantar y baja el contenedor con los siguientes comandos. 
```console
# Levantar el conetenedor
$docker start r-container
# Bajar el contenedor (aunque este comando no es necesario, debido a que si bajas la aplicación se baja el contenedor de forma automática)
$docker stop r-container
```
