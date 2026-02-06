All these types of power supplies are known as [[switching power supplies]] which are known for their efficiency when converting voltage level to another. 
## Buck converter
A buck converter is a step-down converter(steps voltage down) that consists of a inductor, capacitor, and a diode. the idea is that the switching is electronically controlled and has a variable duty cycle. The duty cycle effectively averages out the voltage. for example, if you have a 50% duty cycle then, you will see half the voltage at the output as the voltage is average out ( you see voltage source half the time and the other half you see nothing.) 

![[Buck converter.png| 500]]
The use of the diode is to discharge inductors and capacitors when the switch is not closed in the circuit. This is known as as [[flyback diode]].
- $V_{out} = vin*d$ (d is the duty cycle of the switching frequency)
- $I_{out} =η* \frac{I_{in}}{d}$ (where η is the the efficiency of the converter which is Pout/ Pin)
-