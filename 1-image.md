# Imagen
### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull <nombre imagen> 
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull <nombre imagen>:<tag>
```

Descargar la imagen **hello-world**
# COMPLETAR <img width="1528" height="639" alt="image" src="https://github.com/user-attachments/assets/72c2db4d-792b-4d96-ab60-c2efeaa6e67c" />


**¿Qué es nginx**
# COMPLETAR 
es un servidor web y proxy súper rápido, de código abierto.
Se usa en millones de sitios y aplicaciones porque es ligero, rápido y confiable.

Descargar la imagen  **nginx** en la versión **alpine**
# COMPLETAR <img width="830" height="398" alt="image" src="https://github.com/user-attachments/assets/eac89dc8-1b04-4316-a2a1-113688496ded" />


### Listar imágenes

```
docker images
```

# COLOCAR UNA CAPTURA DE PANTALLA DEL RESULTADO 
<img width="649" height="96" alt="image" src="https://github.com/user-attachments/assets/e0cd5b5d-3aea-4b4a-b2a2-62c1b13c1951" />


**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 
# COMPLETAR
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/9a394f1c-a377-472b-9ebf-f6137579c353" />

**¿Con qué algoritmo se está generando el ID de la imagen**
# COMPLETAR: SHA256

### Filtrar imágenes

```
docker images | grep <termino a buscar>

```

### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi <nombre imagen>:<tag>
```

Eliminar la imagen hello-world 
# COMPLETAR
<img width="822" height="152" alt="image" src="https://github.com/user-attachments/assets/5dd41d1c-e73e-47ff-b502-0de345c95abd" />


-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```
