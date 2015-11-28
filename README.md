# AutoFollowTripod
Tripod able to follow you while you move performing a sport
En la actualidad nos encontramos con situaciones en las que los deportistas necesitan disponer de una grabación de su desempeño, ya que, en infinidad de deportes el uso de estos videos desencadenan una curva de aprendizaje exponencial. Llegados a este punto, esta necesidad requiere de una tercera persona para realizarse. Por ello, nuestras ideas convergen en una misma tarea. La de conseguir un dispositivo capaz de seguirnos y grabarnos durante la práctica del deporte. Gracias a este sistema, resolveríamos la situación farragosa de tener que mandar o pedir a una tercera persona que nos ayude. 

Analizando el mercado nos encontramos con que ya existe una empresa con un proyecto enfocado en nuestra misma dirección. El inconveniente más importante de dicho dispositivo ya patentado, es el económico, ya que, ronda los 800€. Además, por muy alto que sea su precio, sus prestaciones dejan mucho que desear. Y es que la batería del maravilloso aparato únicamente dura 20 minutos. Además, utiliza una cámara ya incorporada, lo que significa que tenemos que utilizar dicha cámara y nos priva de poder utilizar la cámara que queramos y poner una de mayor calidad. 

#Descripción
Nuestro proyecto, mayormente, está enfocado a deportes de riesgo en el que se quieran tomar buenas tomas de video o fotos sin la necesidad de ningún acompañante. También se ha de tener en cuenta que debe de practicarse al aire libre, puesto que  utiliza tecnología gps y esta no funciona en interiores. Por ejemplo, un esquiador se quiere grabar un salto y coloca el trípode a un lado del salto, al empezar a moverse y saltar, la cámara seguirá su movimiento gracias a la señal gps y grabará con totalidad el salto. 
	
#Composición

	Para llevar a cabo este proyecto haremos uso de los siguientes dispositivos electrónicos:

Sensores:
	
Como indicamos anteriormente el sistema hará uso de la tecnología GPS, esta será la encargada de aportarnos información acerca de la posición relativa de la cámara con respecto del deportista. Con esta información obtendremos una posición en el plano XY con el que podremos orientar la cámara hacia donde esté el usuario.

También haremos uso de un IMU (inertial measurement unit), este dispositivo irá montado en la cámara dándonos feedback de hacia donde mira esta. Esto es, nos indicará el movimiento necesario en el plano ZX.

En el dispositivo que portara el usuario (una pulsera), encontraremos al encargado de detectar y medir si el usuario se desplaza en el plano ZX, es decir, si salta. Para esto utilizaremos otro IMU en el cual combinaremos las mediciones de los acelerómetros y la del barómetro para obtener lo deseado.

Para la comunicación entre ambos dispositivos también necesitaremos un sistema inalámbrico, y para ello utilizaremos la tecnología Xbee.

Los microcontroladores elegidos para dar vida al sistema serán los atmega 328p.

Actuadores:

Para el movimiento de la cámara utilizaremos motores paso a paso de 360 pasos.

También utilizaremos una pantalla lcd para que el usuario sepa lo que está haciendo el sistema

Por último también utilizaremos alguno actuadores varios. (pulsadores, botones, leds …)


Funcionamiento

El sistema se encontrará en modo reposo tras encenderlo mediante el interruptor que tendrá incorporado. Una vez se enciendan ambas partes (pulsera, soporte cámara), la pulsera procederá a comprobar si la calidad de la señal gps es adecuada, y así lo indicará mediante unos leds. Cuando haya logrado el estado necesario, los leds se pondrán en verde y en la pantalla LCD se mostrará si el otro dispositivo ha sido encontrado ya. Mientras tanto habrá un led que se mantiene en color rojo. Una vez estén conectados, este led se pondrá en verde, permitiéndonos el uso del botón de calibración con el que activaremos dicho proceso. En el proceso de calibración, la cámara mirará a la posición que está recibiendo de nuestra pulsera y se encenderá en verde el led que se encuentra en la cámara. Tras lograr esto, con unos botones colocados en nuestra pulsera, podremos ajustar la dirección de la cámara para que enfoque mejor. Una vez listo todo esto, podremos empezar a movernos y la cámara nos seguirá.
