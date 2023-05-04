# Prueba Corta #3 y #4

@JoseDanielAcunaSolano-2018145020

[Rpositorio GitHub](https://github.com/JoDaniel1412/evaluaciones-redes)

## 1. ¿Porqué no es posible que cada host en Internet ejecute el algoritmo de Dijkstra para encontrar la ruta mas corta hacia cualquier host en Internet? Explique (20 pts)

Para lograr que todas las maquinas calcularan Dijkstra sería requisito que cada una tuviera un mapa completo con todos los nodos posibles (todos los dispositivos conectados en ese instante al internet), se imposibilita puesto a que hay que estar actualizando constantemente los grafos de cada maquina mientras se gasta poder haciendo el calculo de la ruta más corta en un grafo gigante. Los recursos de la computación actual no dan a basto con esta peticion y menos que
Internet sigue expandiendose.

## 2. Explique el concepto de Hierarchical Routing (20 pts)

Las IPs son mapeadas usando un modelo jerarquico, donde cada cuarteto que la conforma
representa un nivel en la jerarquia, por ejemplo, podriamos decir que todas las IPs que inician con 206 son de Costa Rica, las de 106 de USA y las de 86 son de UK; si tenemos que enviar un paquete a Inglaterra desde CR, sabemos que geofraficamente tenemos que pasar por Miami y luego enviarlo a Europa, gracias a que los paises tienen IPs reservadas podemos encontrar un camino usando esta jerarquia.

## 3. Si tiene la siguiente subred 10.0.0.0/8 y ocupa crear 20 subredes de mínimo 160 hosts, ¿Cual máscara utilizaría? Explique en detalle. (20 pts)

Con una mascara de /25 podemos crear apenas 128 host, por lo que no nos alcanza para los 160 requeridos, ocupamos una mascara /24 que nos permite crear 256host, van a sobrar 94 host que no les vamos a dar uso, pero este es el minimo para el requerimiento.

## 4. El mecanismo de inundación es utilizado para distribuir paquetes de findings/updates (hallazgos) con los vecinos, comente acerca de los mecanismos para evitar que los paquetes se queden por siempre en la red. (20 pts)

Una tecnica es que el paquete vaya con un contador de saltos, es decir la cantidad de routers que ah pasado, despues del salto 30 se destruye el paquete porque se asume que se perdio o que es un duplicado que anda por un camino más lejos

## 5. Para el IP 10.0.39.25/27, calcule los siguientes parametros: (20 pts)

### a. Máscara de subred (ambas notaciones)

La mascara es /27 o 255.255.255.224

### b. Número de red

El numero de red lo calculamos poniendo en cero los primeros 27 bits, es decir 10.0.39.0

### c. Broadcast Address

El Broadcast Adddress se calcula similar, pero seteando los ultimoss 5 bits a uno, es decir 10.0.39.31

### d. Lista de hosts de la red

La lista de hosts son [10.0.39.1 - 10.0.39.30] todas las IPs entre el numero de red y direccion de bradcast
