# Digital-Ammeter
Project Members:
Cherla Pradyumna Reddy (U101116FEC279)
Archana Gujar(U101116FEC158)

Range: 0-1024 mA, resolution 1mA

Abstract: In this project we have aimed to build a digital ammeter with the help of PIC microcontroller. There are no direct methods available to measure current. One of the simplest way to measure is using Ohm’s Law. By finding out the voltage applied and resistance between two nodes we can calculate the amount of current flowing through it. The same methodology is used in this project. We have used PIC16F877a for computational purpose and 8-bit LCD display to view the current value. 

Project Requirements: 
i.	Microcontroller: PIC16F877a
ii.	Op-amp: LM324
iii.	8 Bit LCD Display
iv.	Resistors: 1k (2), 3k (1)
v.	Software: PCW.exe
vi.	Debugger: MPLAB ICE2

Project Layout:



Steps to Follow:
i.	Sense voltage across load resistor and give it as input to the op-amp.
ii.	Amplify the voltage by op-amp.
iii.	Provide output of op-amp to the microcontroller.
iv.	Microcontroller will compute current with the help of known load resistance and divide it by gain factor of op-amp.
v.	Display the value on LCD.

Diagram:


Calculations:
Vout = Vin(1+ R2/R1)
     = Vin(1+3/1)
Vout = Vin(4)        ……… (equ.1)

Op-Amp is used in order to amplify the input voltage as it is very low to measure. The output of op-amp LM324 is connected to the input line AN0 of pic. Voltage value is read at this pin and based on the comparator present inside pic, compared and converted into digital format. But this value is then divided by 4 times to calculate the input voltage (refer equ.1).


