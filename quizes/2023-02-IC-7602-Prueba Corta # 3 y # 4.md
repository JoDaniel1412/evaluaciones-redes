# Prueba Corta #3 y #4

@JoseDanielAcunaSolano-2018145020

[Rpositorio GitHub](https://github.com/JoDaniel1412/evaluaciones-redes)

## Explique el concepto de colisión durante el proceso de asignación del canal, comente las diferencias entre medios guiados y medios no guiados

Cuando en una red multiples dispositivos envian paquetes al mismo tiempo se puede dar
una colision; los medios guiados son los de cable, ya que su señal se mueve a lo largo
de un camino, reciben poca interferencia y son muy fiables; en cambio los medio no
guiados son los inalámbricos, que tienen altas perdidas de paquetes, las señales viajan
en el aire o espacio, tienen la ventaja de ser convenientes al atravesar superficies y
tener infraestructura centralizada. Ejemplos:

Cable:

- Coaxial
- Fibra optica

Inalambricos:

- WiFi
- Radio Am/FM

## ¿Como funciona el algoritmo de asignación del canal Aloha y Aloha Ranurado? Explique

El Aloha es un algoritmo que permite sincronizar torres de radio, funciona enviando un
mensaje sin esperar permiso, luego el receptor envia una señal de recibido, si el mensaje
se perdio, la terminal emisora espera un tiempo determinado antes de volver a intetar; este
algorithmo es propenso a colisiones, por lo que se creo una versión mejorada, el Aloha
Ranurado, que utiliza intervalos de tiempo para enviar los mensajes y así disminuir las
probabilidades de colisión.

## ¿Cuáles son las diferencias entre Hub y Switch? ¿Porqué razón el Switch es mejor?

El Hub tiene la desventaja de que envia las señales a todos los dispotividos
conectados, sin importar si el mensaje tenía ese destino o no, impactando
negativamente el rendimiento, seguridad. Los Switches resuleven estos problemas
pero involucran un mayor costo, otra ventaja del Switch es que puede regular el trafico
en la red, además de las mejoras en rendimiento y seguridad.

## ¿Es posible transportar tramas Ethernet embebidas en imágenes PNG? Justifique su respuesta.

Si se desallorra un protocolo para definir el formato de las imagenes que se van a enviar,
para que tanto el emisor como el receptor puedan interpretarlas como es intencionado, si se
pueden enviar estas tramas. Eso es un protocolo, un estandar de reglas definidas para
concordar como se transmite e interpreta la información.
