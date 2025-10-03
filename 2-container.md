# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
# COMPLETAR
<img width="649" height="89" alt="image" src="https://github.com/user-attachments/assets/3a972bc6-21c0-4cff-96da-387d703b4bd3" />


Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world
# COMPLETAR
<img width="670" height="65" alt="image" src="https://github.com/user-attachments/assets/325c80ff-bf08-4fea-85f0-47b28e2d08ef" />


### Listar los contenedores ejecutándose o no

```
docker ps -a
```

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 
# COMPLETAR
<img width="1071" height="128" alt="image" src="https://github.com/user-attachments/assets/1aaa4a67-031e-464d-9b1b-3eb939d4830a" />


### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```

### Para detener un contenedor

```
docker stop <nombre contenedor>
```

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
# COMPLETAR
<img width="1528" height="796" alt="image" src="https://github.com/user-attachments/assets/b4be7cf3-d623-49f2-a081-20498ea72647" />


**¿Qué sucede luego de la ejecución del comando?**
# COMPLETAR  
Se queda ejecutnado el contenedor.

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
# COMPLETAR
<img width="955" height="294" alt="image" src="https://github.com/user-attachments/assets/60cf4ca2-a322-4112-b101-e3d8706729ed" />


### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
# COMPLETAR
<img width="1437" height="538" alt="image" src="https://github.com/user-attachments/assets/a6b53bd1-6339-420f-9514-3d6beae852f8" />


Verificar que el contenedor que se eliminó
# COMPLETAR
<img width="1437" height="538" alt="image" src="https://github.com/user-attachments/assets/eb93a577-9050-47ad-8ce0-c929d103b067" />


### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 
# COMPLETAR
<img width="1437" height="538" alt="image" src="https://github.com/user-attachments/assets/50b7e3fc-6ccf-4702-9b9e-be28794d13cc" />


Verificar que el contenedor que se eliminó
# COMPLETAR
<img width="1437" height="538" alt="image" src="https://github.com/user-attachments/assets/3c6545d1-3c20-4559-9f26-e018b5c07996" />


### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
# COMPLETAR
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/4d5303a7-bc34-47ce-bfcb-96d6bf7937e7" />

