impedance is similar to resistance but with the introduction of non LTI([[linear time invariant(TODO)]]) components that are also considered. Impedance is the measure of the opposition to electrical flow. The format of impedance can be seen below
![[Impedance equation.png]]

- Z = impedance 
- R = Real component (basically resistance)
- jX = imaginary part/reactance( note that J is an imaginary number(i))
-  the unit of impedance is ohms Ω

impedance can also be described as a right triangle which can be seen in the picture below![[impedance triangle.png|600]]
note that this implication means that the impedance is actually the magnitude of the resistance and the reactance

## different impedance representations
since there are two different equations they that describe the same thing that means each one describes different information.  $Z = R + Jx$ $maintains the phase information which is described in the reactance part. Whereas, the magnitude of z describes the whole circuits opposition to current. Typically you may see $Z = r +jx$ more often as phase information can be useful in understanding how signal will interact with the circuit. 

## Reactance
Reactance is the major difference in impedance and reactance which makes impedance a little more complicated.

| component | unit | reactance       |
| --------- | ---- | --------------- |
| capacitor | F    | $\frac{1}{jwc}$ |
| inductor  | H    | $jwl$           |

resistance is only part of the real so we wont see any influence from a resistor in the reactance .
 J is the imaginary number, note that typically J should always be brought to the numerator if possible which means you can use this property for the capacitors reactance
 ![[re-arranging capacitor reactance.png]]
 so you can think of capacitor reactance as $z = -\frac{j}{wc}$ . 
- C is the capacitance (in Farads) of the capacitor
- L is inductance( in Henrys) of the inductor
- ω is angular frequency which is also ($2πf$)
##  impedance practice
### RC circuit
this is a RC(resistor and capacitor) circuit in series to find the impedance we follow [[Parallel and series Resistance]] rules. In this particular case we follow series rules as it is a series circuit note that 1000 is the Frequency of the circuit.
![[RC series circuit.png]]  


#### Solution
![[RC impedance example solved.png]]
$$ Z = 1000 - J1591.55 Ω$$
#### checking answer with simulation

![[impedance simulation check.png]] using LTSpice we can use traces and [[Ohm's law]] to find the impedance of the circuit at a certain frequency(1K ). We know that the total resistance could be found if you did $$R_{total} = \frac{V_{total}}{ I_{total}}$$
so by using a custom trace that does the total voltage divided by the total current of the circuit and looking at the value at around 1Khz we can find the resistance of the circuit. The picture shows that that real part is 1000Ω and the imaginary(reactance) of the circuit at 1Khz is 1.5856KΩ
which is rather close to the 1591.55 we calculated. The deviation is mostly likely due to the fact that the frequency isn't exactly 1Khz but very close to it

## RL circuit
![[series RL circuit practice.png]]

![[RL series problem work.png]]

![[Pasted image 20250608173206.png]]![[RL series sim.png]]

the simulation supports the numbers that were obtained by hand with some deviance that could be chalked down to the the fact that frequency is at 999.6 not 1k