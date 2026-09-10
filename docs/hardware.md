Como todo sistema robotico ProMice cuenta con componentes actuadores, estructuras mecanicas de soporte, estructuras articuladas, sistema de transmision de movimiento, electronica e instrumentacion. A continuacion presentamos una descripcion general del hardware de ProMice. Detalles sobre los materiales y ensamblajes pueden ser consultados en la seccion [Tutorial](3D_printing.md).

# Actuators and their suport
El sistema cuenta con 4 motores a pasos Nema 17 como actuadores que sostienen en un soporte de impreso en 3D con PLA. Los motores tienen instalada una polea impresa en resina con un sistema de tension para los cables de actuacion. 

![Motors and rack](images/motors_rack.jpg){ width=70% .center}
# Transmission and articulations system 
ProMice es un cable-driven system que usa un Bowden-cable-type system como sistema de transmision de movimiento. El cable actuador es un fino cable metalico y el conducto es [PTFE Tube](https://fr.vwr.com/store/product/576865/null).



![Bowden actuation](images/front_bowden.jpg){ width=70% .center}

![PCB teensy](images/PCB_teensy.jpg){ width=50% .center}

![Hall sensors socket and elbow](images/hall_sensors_socket.jpg){ width=50% .center}

![uSteppers](images/uStepper_drivers.jpg){ width=50% .center}

The precision of the prosthesis movement is achieved through stepper motors equipped with controllers and Hall sensors.
This allows for rotations of much less than 1 degree and a high sampling rate for the angular position of the actuators

show the cable driven sistem
