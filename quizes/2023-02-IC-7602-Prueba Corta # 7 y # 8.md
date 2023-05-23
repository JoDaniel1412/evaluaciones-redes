# Prueba Corta #7 y #8

@JoseDanielAcunaSolano-2018145020

[Rpositorio GitHub](https://github.com/JoDaniel1412/evaluaciones-redes)

1. Lucky Starr Tech se encuentra desarrollando un protocolo que permita el envío de datos sobre un medio poco confiable, este medio puede verse afectado por radiación electromagnética de aparatos y otros medios de comunicación. En calidad Ingeniero o Ingeniera en telecomunicaciones, a usted se le ha encargado diseñar la trama que será utilizada por el protocolo, algunos detalles importantes (70 pts)

   - Los identificadores de destino y fuente tienen un total de 6 octetos cada uno.
   - El tamaño máximo del payload (datos) que puede llevar la trama es de 160 bytes, esto debido a que tramas muy grandes pueden causar muchos problemas.
   - El contenido puede ir encriptado con llave pública/privada.
   - Se debe garantizar la entrega en orden de las tramas.
   - Se debe verificar que los datos estén correctos.
   - Se debe tomar en cuenta que pueden existir diferentes tipos de tramas.
   - Se debe hacer una propuesta con trama de tamaño variable (entre 0 y 160 octetos) y otra con trama de tamaño fijo.
   - El header incluyendo la verificación debe ser lo más pequeño posible, se debe trabajar bajo el supuesto de que la trama debe ser lo más peque posible. Su propuesta debe hacer un uso eficiente del espacio, de especificar cuántos bits se van a usar por campo en su trama.

## Protocolo de tamaño fijo

|                     |                |                   |
| ------------------- | -------------- | ----------------- |
| destination (6 oct) | source (6 oct) | position (2 oct)  |
| checksum (2 oct)    | type (1 oct)   | payload (160 oct) |
|                     |                |                   |

- Para la encriptacion con llave no se ocupa nada porque ya fue enviada en otro paquete
- Para garantizar el orden de las tramas se envia el _position_
- La verificacion de los datos se realiza mediante un _checksum_
- El _type_ indica el tipo de trama

## Protocolo de tamaño variable

|                     |                  |                  |
| ------------------- | ---------------- | ---------------- |
| destination (6 oct) | source (6 oct)   | position (2 oct) |
| type (2 oct)        | checksum (2 oct) | length (2 oct)   |
| payload (0-160 oct) |                  |                  |
|                     |                  |                  |

- Se agrega un valor _length_ porque es una trama variable

1. Explique detalladamente la razón por la cual Internet Protocol se implementa como un servicio sin conexión en lugar de un servicio orientado a conexión (30 pts).

Para que se pueda hacer un servivio orientado a conexion es necesario que se mantenga una coneccion permanente mientras se intercambian los datos lo cual consume mayor cantidad de recursos que una conexion volatil que solo escucha y transmite cuando es necesario.

Si internet fuese orientado a conexion se imposibilitarian implementar otro tipo de conexiones como UDP, ya que esta implementacion no funciona a la inversa.

Al no ser una conexion continua la informacion se envia en paquetes, que facilita el manejo de errores mediante tecnicas de _wait & retry_, si se pierde un paquete se puede reenviar y no perder todos los datos.
