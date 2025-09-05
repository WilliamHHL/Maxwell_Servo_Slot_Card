## Features:PH sensor, Pump(12V), PTZ Camera, Servo Control, UART switches, CAN BUS.

# To instruct the board  

0x1A： P1H, P1L,  P2H, P2L,  P3H, P3L,  P4H, P4L  
0x1B： P5H, P5L,  P6H, P6L,  P7H, P7L,  P8H, P8L  
0x1C： BTN1, BTN2, BTN3, BTN4, BTN5, BTN6, BTN7, BTN8

0x20: "?<SENSR>"  example: 0x20: ? PH \0 \0 \0 \0 \0  
0x20: "!<SENSR>:<DATA>"  example: 0x21: ! PH : fi4, fi3, fi2, fi1 

1A ,1B are the servos,P1H is the HIGH byte of pwm1,P1L is the low byte etc.  
1C is pump(BTN1,only 1 or 0)  
0x20 is the PH sensors,using IEEE754 representations (Big Endian)

0x18 is the PTZ:  
SXIO4 is the mode and sensitivity  
SXIO5 is the pitch  
SXIO6 is the head  

<B> Connections:  
SX-IO2 is used for pump(12V)  
SX-IO7 is used for ADC(the PH sensor)  

Designed for MATE ROV
