# Series
circuits that are in series means that the [[nodes]] of either side of the component connect to two different components on either side.
![[Series Resistance.png]]
Series circuits make a single path that the current can go through.  Some of the properties of series circuit are:

| Unit    | Behavior                                                                                                                                                                           |
| ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Voltage | Each component will have a different voltage through it and the sum of all voltages through each component is the total voltage that goes through the start of the series circuit. |
| Current | The same amount of current will go through each component in the series circuit.                                                                                                   |

To find the voltage through each component you just need to use [[Ohm's Law]] to calculate each voltage through the component . R is the resistance of the component you want to find the voltage through and the current is the total current that is going through the series circuit

To find the current through the series circuit you need to first find the [[Equivalent Resistance]] of the series circuity then you can use [[Ohm's Law]] rearranged to solve for current where the voltage is the voltage through the resistor and the resistance if the equivalent resistance.

## finding series resistance
the simplest of the two resistances. You just need to add the resistances together
$$R_{eq} = R_{1} + R_{2} + R_{3} + ... + R_{n} $$ Where $R_{eq}$ is the total resistance in the series circuit

## finding parallel resistance
a little more complicated to calculate resistances 
$$\frac{1}{r_{eq}} = \frac{1}{R_{1}} + \frac{1}{R_{2}} +\frac{1}{R_{3}} + ... + \frac{1}{R_{n}}$$
there is a rule of thumb/technique where you can group your parallel resistances into groups of 2s 
and use a different modified version of the equation above to make it more simpler to calculate.
$$ R_{eq} = \frac{R_{1}*R_{2}}{R_{1} + R_{2}}$$
this is a easier equation to solve so if you group your parallel resistances into two you can keep on using this equation to simplify parallel resistances until you have one resistances.![[parallel resistor example.png]]
the circuit can be simplified by using the using either of the two equations to solve for the resistance
$$\frac{1}{r_{eq}} = \frac{1}{4.7k} + \frac{1}{4.7k} + \frac{1}{4.7k}+ \frac{1}{4.7k}$$
or you can  divide it into
$$ r = \frac{4.7k * 4.7k}{4.7k + 4.7k}$$
this will combine two of the parallel resistor with a value of r (in this case 2.35k) into one then you will have three resistors. You can keep on doing this until you have 1 resistor which will give you the $R_{eq}$ value.