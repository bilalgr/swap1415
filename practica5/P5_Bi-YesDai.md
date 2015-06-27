# Práctica 5
## 0 - Configuracion de red de las máquinas :
Máquina 1:  192.168.32.128

Máquina 2:  192.168.32.129

## 1- Crear una BD con una tabla y algunos datos:

![imagen1_1](https://github.com/bilalgr/swap1415/blob/master/practica5/img_1-1.PNG)



## 2- Realizar la copia de seguridad de la BD completa usando mysqldump.

![imagen1_2](https://github.com/bilalgr/swap1415/blob/master/practica5/img_1-2.PNG)


## 3- Restaurar dicha copia en la segunda máquina (clonado manual de la BD).

![imagen1_3](https://github.com/bilalgr/swap1415/blob/master/practica5/img_1-3.PNG)

![imagen1_4](https://github.com/bilalgr/swap1415/blob/master/practica5/img_1-4.PNG)

## 4- Realizar la configuración maestro-esclavo de los servidores MySQL para que la replicación de datos se realice automáticamente.

### 1- Configuración del maestro:

Configuramos el archivo de configuración de mysql usando nano : nano /etc/mysql/my.conf

Comentamos el parámetro bind-address que sirve para que escuche a un servidor:

 #bind-address 127.0.0.1

Le indicamos el archivo donde almacenar el log de errores. De esta forma, si por ejemplo al reiniciar el servicio cometemos algún error en el archivo de configuración, en el archivo de log nos mostrará con detalle lo sucedido:

log_error = /var/log/mysql/error.log

Establecemos el identificador del servidor:

server-id = 1

El registro binario contiene toda la información que está disponible en el registro de
actualizaciones, en un formato más eficiente y de una manera que es segura para las
transacciones:

log_bin = /var/log/mysql/bin.log

finalmente reiniciamos el servicio:

service mysql restart

![imagen1_5](https://github.com/bilalgr/swap1415/blob/master/practica5/img_1-5.PNG)


### 2- Configuracion de esclavo:

![imagen1_6](https://github.com/bilalgr/swap1415/blob/master/practica5/img_1-6.PNG)

### 3- Creación de un usuario para la BD denominado esclavo en la maquina de maestro:

![imagen1_7](https://github.com/bilalgr/swap1415/blob/master/practica5/img_1-7.PNG)

![imagen1_8](https://github.com/bilalgr/swap1415/blob/master/practica5/img_1-8.PNG)


### 4- Configuración de datos del maestro en el esclavo:

![imagen1_9](https://github.com/bilalgr/swap1415/blob/master/practica5/img_1-9.PNG)

### 5- Comprobación de que todo va bien:

![imagen1_10](https://github.com/bilalgr/swap1415/blob/master/practica5/img_1-10.PNG)

### 6- Insertamos una tupla en el esclavo y comprobamos si la tabla se ha actualizado en el esclavo:

![imagen1_11](https://github.com/bilalgr/swap1415/blob/master/practica5/img_1-11.PNG)
![imagen1_12](https://github.com/bilalgr/swap1415/blob/master/practica5/img_1-12.PNG)
