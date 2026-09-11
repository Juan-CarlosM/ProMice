# 3D printing 
ProMice is made up mostly of 3D-printed parts. Two very common prototyping techniques are used:
PLA filament printing and resin printing

![prothesis full](images/Prosthesis_full.png){width=70% .center}

Now let's describe each of the parts and their function. Each description also shows the print orientation for best results.

## Resin-printed parts
Resin-printed parts are those that require the highest level of detail and quality; they are also the smallest parts.
To print the resin parts, we used the [Form 4 Printer](https://formlabs.com/3d-printers/form-4/) and the
general-purpose [gray resin](https://formlabs.com/products/grey-resin/). This resin offers a good balance of mechanical properties, particularly
a soft response to friction and a detailed finish.

The printer settings for layer height are the default ones.

![layer thickness](images/layers_thickness.png){ width=70% .center }

![grey resin](images/grey_resin.png){ width=50% .center }


The image below shows the 3D model of the parts that are printed in resin. These are the front assembly that houses the joints and the pulleys with their
tensioning system for the actuating cables.

![Resin parts](images/resin_parts.jpg){width=70% .center}



### The forearm 

![forearm 3D](images/forearm_3D.png){width=60% .center}

The forearm es la extremidad del sistema porque no hay articulacion de muneca, which means there is a hand but there is not wrist joint. 
La punta de los dedos es punto del efector final, esta hecha mediante el escaner de una pata real de raton
por lo que sus dimensiones respetan las de una pata de raton real, en los dedos se pueden ver pequenas cavidades para los cables de un sensor 
capacitivo, la idea es poder detectar el tacto de forma puntual. 
La parte trasera tiene una cavidad para instalar el [sensor hall](https://www.ti.com/product/TMAG5273?qgpn=tmag5273) o encoder. La cavidad 
esta alineada con el eje de rotacion del codo y justo a la altura del eje tenemos las cavidades para insertar the
elbow ball bearings. Ortogonales al eje de rotacion de la articulacion se encuentran 
los dos agujeros por dond epasan los actuating cables que dirigen la articulacion.



![forearm labels](images/forearm_labels.png){width=60% .center}

![forearm resin](images/forearm_resin.jpeg){width=30% .center}
 
Orientation for 3D printing :
![forearm printing](images/forearm_printing.png){width=30% .center}

### The ball-arm of the ball joint

![ball arm 3D](images/ball_arm_3D.png){width=60% .center}

El diseno de esta pieza y sus dimensiones estan detallados en la seccion [Mechanical design](mechanical_design.md). se trata de la bola
de la ball joint. esta bola esta seccionada de la cual la parte mas frand erepresenta un 70% d ela esfera aproximadamente.
La seccion grande tiene cavidades para integrar lo que llamamos [Yaw-lock system](mechanical_design.md#yaw_lock_system).
El resto es una especie de tapa para completar la esfera. Aunque tiene un diametro de 8mm su diseno  la vuelve relativemnnte sencilla 
de ensamblar.


![ball arm labels](images/ball_arm_labels.png){width=70% .center}

![ball arm resin](images/ball_arm_resin.jpeg){ width=30% .center}

add 3D model, the printing orientation and resin model
description of the piece cleanine etc.

the arm of the ball is a stick with a design in the lower part that allws the attachment of the actuating cables. 
Tambien tiene una cavidad longitudinal al brazo en l aque se inserta la varilla que sostiene la articulacion del codo. 
cercano al brazo tambien tiene 4 agujeros cuyo proposito se detalla en la seccion de [Encoders linearization](encoders_linearization.md)
 
Orientation for 3D printing :
 
![ball_arm_printing](images/ball_arm_printing.png){width=50% .center}

 
### The socket

![socket 3D](images/socket_3D.png){width=60% .center}

El socket tambien esta dividido en dos piezas para poder ensamblarse con la bola y usamos un anillo para mantener las dos piezas juntas.
En ambas piezas podemos notar diferentes ranuras y cavidades. La pieza uno es la mas grande, tiene 9 cavidades cilindricas de las cuales 8 estan 
distribuidas radial y simetricamente y una esta en el centro.
En las 8 cavidades radieales se inserta un [PTFE Tube](https://fr.vwr.com/store/product/576865/null) with an internal diameter of 0.3mm 
and external diameter of 1.5mm para reducir el radio y por lo tanto el back lash de los actuating cables. En l acabidad esferica 
que alberga la bola cuenta con un housing donde se inserta un mini rodamiento que forma parte del [Yaw-lock system](mechanical_design.md#yaw_lock_system).
Justo en el centro se encuentra la cavidad del ball joint hall sensor que medira el movimiento de la articulacion. Esta cavidad esta
conectada a la novena cavidad cilindrica para pasar los cables del sensor. 


![socket labels](images/socket_labels.png){width=60% .center}


La otra parte de socket es simetrica a la parte baja de la primera, con la excepcion de que esta no alberga rodamiento su funcion es 
contener la esfera en conjunto con la pieza uno. The socket includes a ring thar fastens the two pieces toguether 


![Socket parts](images/socket_parts.jpeg){ width=40% .center } 
 
Orientation for 3D printing :
  
![socket_printing](images/socket_printing.png){width=70% .center}


### Shoulder ball bearing housing

![shoulder ball bearing housing 3D](images/shoulder_ball_bearing_housing_3D.png){width=80% .center}

This section is composed by 3 piece. it holds the shoulder Z-axis rotation system. It has housings for two ball bearings and two cavities for the PTFE tube. La pieza mas gra,de es la
parte que sostiene la parte frontal de la protesis, en la imagen de abajo se muestra senalado el front support hole para apoyar la protesis en un
[Flex arm](https://www.amazon.fr/SMALLRIG-Articul%C3%A9-Friction-R%C3%A9glable-Moniteur/dp/B08B63WXWN/ref=sr_1_1?crid=36M1VY295M2MQ&dib=eyJ2IjoiMSJ9.KGiIRm_QPLJhUIhU1N34kqAYeY66ar65T2RxIAyC5f-uMuk5aTKTYd3H7nni7IM6WjRBQcNbQ9WdEJuWjIoZFVrEm2gYyOMpcHyqmOA4SWdRUADsrTYoYQMwC7yEsQ6xcVR144ers6Tz1gCvJFgjxIjzeC-KBF_7Zjg-uiVb4PxhTXkaV829QS1jBANfmplZqVrv-mAeqohvgv2w3wQRbfktaMZ0KMstzPFnAle9ixHhLMXd_0YWc8hwDBu47y6c5cgRjOTXP1nDM0HJygyaWxgcuB6_G2oyH0hdsHEWegw.Qr0gYVoHgxusC7XTGdkxMi8Gfpx3oLuNlquboS8tCac&dib_tag=se&keywords=bras%2Bmagique&qid=1786965479&sprefix=braz%2Bma%2Caps%2C147&sr=8-1&th=1).

 
![shoulder ball bearing housing labels](images/shoulder_ball_bearing_housing_labels.png){width=70% .center}

Las dos piezas restantes son complementos para sostener los rodamientos y para sostener el  [PTFE Tube](https://fr.vwr.com/store/product/576865/null)


![shoulder case 2 resin](images/shoulder_case_2_resin.jpeg){ width=40% .center }

faltan imagenes en resina de las otras dos piezas 
 
 Orientation for 3D printing :
  INSERER IMAGE
![shoulder ball bearing housing](images/shoulder_ball_bearing_housing.png){width=70% .center} 


### Shoulder rotatory pieces 
![shoulder rotatory pieces 3D](images/shoulder_rotatory_pieces_3D.png){width=60% .center}

Este es un set de tres piezas que transmiten la rotacion en Z del hombro al resto d ela protesis. La pizea en el top va insertada en la polea, 
tiene una cavidad para un iman que queda justo debajo de un encoder para medir la rotacion. La polea lleva atados los actuating cables 
como lo muestra the red dashed line en la figura de abajo. La pieza de mas abajo es la conexion entre la polea y el socket.  

![shoulder rotatory pieces labels](images/shoulder_rotatory_pieces_labels_v2.png){width=85% .center}
 
Orientation for 3D printing :
  
![shoulder rotatory pieces printing](images/shoulder_rotatory_pieces_printing.png){width=70% .center} 
### Top encoder base. 
![top encoder base 3D](images/top_encoder_base_3D.png){width=60% .center}

Esta ultima pieza sostiene un uStepper driver para medir la rotacion del hombre en el eje Z 

![top encoder base](images/top_encoder_base.png){width=45% .center}

![top encoder base](images/top_encoder_base_resin.jpeg){width=45% align=left}

![top encoder base printing](images/top_encoder_base_printing.png){width=45% .center}

### Pulleys
![pulley views](images/pulley_views.png){width=75% .center}



<p style="color: #999999;">There are four pulleys in total, each mounted on a motor. They are used to transmit the motors’ rotation to the prosthesis, allowing it to move along its different axes. Motion is transmitted via wires, which are attached to the end of the prosthesis on one side and wound around the pulley on the other, as shown below:</p>

![pulley cable](images/pulley_cable.png){width=75% .center}

<p style="color: #999999;">The tension of the wires can be adjusted by turning the corresponding screw: turning it clockwise increases the tension on the wire, while turning it counterclockwise decreases it.</p>


![pulley screw](images/pulley_screw.png){width=75% .center}
 
Orientation for 3D printing :
 
![pulley printing](images/pulley_printing.png){width=70% .center}

## impresion con PLA

The motors rack and PCB housing are printed in PLA, this pieces do not require a high level of precision. PLA also produces less brittle parts, which is essential for supporting the weight of the motors.
![PLA parts](images/PLA_parts.jpg)

Orientation for 3D printing :
![motors suport](images/motors_suport_printing.png){width=70% .center}
 
![teensy suport printing](images/teensy_suport_printing.png){width=50% .center}
