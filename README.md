# Laboratorio Robotica Industrial, Entradas y Salidas

# Miembros:
Edgar Giovanny Obregon Espitia

Juan Nicolas Carvajal Useche
# Descripción de la solución planteada
En este documento se describe el procedimiento para llegar a la solución mostrada en los videos
de simulación y de implementación.
1. Simulación en RobotStudio
El primer paso fue crear las trayectorias requeridas para la práctica, la trayectoria de escritura ya
estaba creada desde la práctica anterior, por lo que en esta ocasión solo se creó la trayectoria para
posicionar en mantenimiento de la herramienta. La pose del robot al final de esta trayectoria se
puede observar en la figura 1.

![image](https://github.com/Ggio0/Lab2/assets/82681128/80dd2b25-afb8-4762-b0fb-c16a8560790b)

Figura 1. Pose final del robot en la trayectoria de mantenimiento.

Con las trayectorias creadas, el siguiente paso fue crear las señales correspondientes para las
entradas y salidas digitales, la sintaxis en este caso es: DO_XX para el pin XX de salida digital y DI_YY
para el pin de entrada digital YY, dado que la práctica solo requería 2 entradas y 2 salidas, se
definieron las señales mostradas en la figura 2.

![image](https://github.com/Ggio0/Lab2/assets/82681128/9d789688-e793-4024-b27c-dbbbee1f86be)

Figura 2. Entradas y salidas digitales definidas en simulación.

Con estas señalas creadas, y las trayectorias, se escribe en el MAIN el código que ejecuta en bucle
el programa, este se observa en la figura 3.

![image](https://github.com/Ggio0/Lab2/assets/82681128/c1f11663-4197-4612-9464-234986254970)

Figura 3. Código del MAIN del programa.

Se observa que se usa el condicional IF que verifica la entrada que se ha pulsado, y dependiendo de
esto entra a la rutina de escritura o de mantenimiento, a su vez, este código se deja en bucle usando
el GOTO inicio para que constantemente revise las entradas digitales. Cuando el usuario active una
entrada digital se entrará a la rutina, en la figura 4 se observa el código implementado.

![image](https://github.com/Ggio0/Lab2/assets/82681128/067a80a5-e05a-4bba-acb6-7da4247cb399)


Figura 4. Rutinas de movimiento de escritura y mantenimiento.

Se observa que cuando se entra a la rutina, primero, se usa “Set DO_XX” para encender la salida
correspondiente según lo solicitado en clase, y después de esto se usa “Reset DO_XX” para apagarla.
En este lapso, se ejecutan las rutinas con las trayectorias creadas.
Para probar en simulación, se usó el simulador de entradas y salidas, los resultados se pueden
evidenciar en los videos anexos de simulación.
3. Implementación en laboratorio
El primer paso en el laboratorio fue identificar y conectar las entradas y salidas del tablero de control,
para este proceso se probó continuidad en los cables desde el controlador del robot (en su módulo
de entradas y salidas) y los cables del tablero, de esta manera y leyendo la hoja de datos del módulo,
se identificó cuáles eran entradas, cuáles salidas y los pines de alimentación. De esta manera, las
figuras 5 y 6 muestran físicamente los pines de entrada y salida dispuestos para esta práctica.

![image](https://github.com/Ggio0/Lab2/assets/82681128/88bff725-45e3-4278-91bd-72dd3fa84e37)


Figura 5. Estructura interna del tablero de control.

![image](https://github.com/Ggio0/Lab2/assets/82681128/3580c8a4-ee6b-4d06-a5db-cc0b6825ac78)


Figura 6. Elementos físicos asignados a las salidas y entradas


Tras haber conectado estos dispositivos al módulo de entradas y salidas del controlador, se cargó el
programa mediante una usb al FlexPendant, aquí lo primero fue poner en el laboratorio físicamente
el workobject (tablas y soportes con la hoja) y la herramienta al robot. Después, se calibró el robot
usando el método de los 3 puntos, es decir, moviendo manualmente la herramienta a 3 puntos en
la hoja en la que se va a escribir. Esto se evidencia en la figura 7.

![image](https://github.com/Ggio0/Lab2/assets/82681128/b4712c24-1862-464b-ae7c-89e4f6e72058)


Figura 7. Movimiento manual del robot a puntos sobre la superficie de la hoja.

Con esta información, se calibra el robot y posteriormente se ejecutan los programas. Los resultados
se pueden evidenciar en los videos anexos en el repositorio.

# Codigo en Rapid
Programa en robot studio usado para el desarrollo de la practica.

https://github.com/Ggio0/Lab2/tree/main/Entregables/CodigoRAPID

# Video 
Video del robot vista 1.

https://github.com/Ggio0/Lab2/assets/82681128/0f652e26-4e41-4d36-beff-1bacdffa7c71

Video del robot vista 2.

https://github.com/Ggio0/Lab2/assets/82681128/0958e687-3ede-4e31-b915-f33050a5090f


Video de la simulacion.



https://github.com/Ggio0/Lab2/assets/82681128/c3d6b985-d46b-4608-a283-8335500bc076



ver en mejor calidad.

https://github.com/Ggio0/Lab2/tree/main/Entregables/Videos

