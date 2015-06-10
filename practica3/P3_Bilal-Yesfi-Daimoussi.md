# Práctica 3
## 0 - Configuracion de red de las máquinas :
Máquina 1:  192.168.32.128

Máquina 2:  192.168.32.129

Balanceador Nginx: 192.168.32.130

Balanceador Haproxy: 192.168.32.133

## 1- Instalación y configuración de Nginx como balanceador de carga: 
### 1-1 Instalación de Nginx:

![imagen4_0]((https://github.com/bilalgr/swap1415/blob/master/practica3/Capture4_0.PNG))

### 1-2 Configuración de Nginx como balanceador de carga usando algoritmo de round-robin:

![imagen4_1](https://github.com/bilalgr/swap1415/blob/master/practica3/Capture4_1.PNG)


### 1-2 reinicio de Nginx:

![imagen4_2](https://github.com/bilalgr/swap1415/blob/master/practica3/Capture4_2.PNG)

### 1-3 Comprobación del funcionamiento:

![imagen4_3](https://github.com/bilalgr/swap1415/blob/master/practica3/Capture4_3.PNG)

### 1-4 Configuración de Nginx como balanceador de carga usando algoritmo con ponderación:

![imagen4_4](https://github.com/bilalgr/swap1415/blob/master/practica3/Capture4_4.PNG)

### 1-5 reinicio de Nginx:

![imagen4_2](https://github.com/bilalgr/swap1415/blob/master/practica3/Capture4_2.PNG)

### 1-6 Comprobación del funcionamiento:

![imagen4_6](https://github.com/bilalgr/swap1415/blob/master/practica3/Capture4_5.PNG)

## 2- Instalación y configuracion de Haproxy como balanceador de carga:

### 2-1 Instalación de Haproxy:

![imagen3_1](https://github.com/bilalgr/swap1415/blob/master/practica3/Capture3_1.PNG)

### 2-2 Configuración de Haproxy como balanceador de carga usando algoritmo de round-robin:

![imagen3_2](https://github.com/bilalgr/swap1415/blob/master/practica3/Capture3_2.PNG)

### 2-3 Salvar la configuración:

![imagen3_3](https://github.com/bilalgr/swap1415/blob/master/practica3/Capture3_3.PNG)

### 2-4 Comprobación del funcionamiento:

![imagen3_4](https://github.com/bilalgr/swap1415/blob/master/practica3/Capture3_4.PNG)

### 2-5 Configuración de Haproxy como balanceador de carga usando algoritmo con ponderación:

![imagen3_5](https://github.com/bilalgr/swap1415/blob/master/practica3/Capture3_5.PNG)

### 2-6 Comprobación del funcionamiento:

![imagen3_6](https://github.com/bilalgr/swap1415/blob/master/practica3/Capture3_6.PNG)

Vemos que es verdad que manda el trabajo al servidor con mayor peso pero no lo hace como Nginx.
