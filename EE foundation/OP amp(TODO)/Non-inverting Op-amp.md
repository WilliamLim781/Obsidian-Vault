
Common op-amp topology that is used to apply a fixed amount of gain to an signal while keeping the phase of the signal that same. The Falstad simulation demonstrates the circuit layout and the behavior of said circuit. In the simulation, the red signal is the input signal and the green signal is the output signal.
![[Non-inverting Op-amp.png]]

the equation to calculate how much gain this topology will apply to a signal is
$$V_{out} = (1 + \frac{R_{f}}{R_{in}})V_{in}$$
where $V_{out}$ is  the output signal,$R_{f}$ is the feedback resistor which is the resistor connected in the feedback system, $R_{in}$ is the input resistor which is the resistor which is connected to the negative terminal. With the simulation above we can plug in the values and get that the gain(Vout/Vin) you get 2 which is supported by the simulation as the input 5v is now 10v.

Notice that with the non-inverting op amp you will always have a gain that is greater than 1 since you have the +1 in the equation. So if you needed to lower the gain of a signal you couldn't use this topology as it cannot have a gain less than 1.