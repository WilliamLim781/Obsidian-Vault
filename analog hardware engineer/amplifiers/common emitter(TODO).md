![[common emitter bjt.png|500]]



common emitters are defines as a [[BJT(TODO)]] that has a that as the input at the base of the transistor, ground connected to the emitter and a resistor connected to the voltage source and the collector of the transistor. The output is taken in between the transistor and the resistor

There is another version of this amplifier but with  something known as [[degeneration(TODo)]]. The introduction of degeneration allows for more stability and a reduced dependency on $g_{m}$ which is innate feature that varies from BJT to BJT.  Below is a table the demonstrates

![[common emitter with degeneration.png]]



Below is a table that compares the two different circuits

| characteristics | with emitter degeneration                                                        | without emitter degeneration |
| --------------- | -------------------------------------------------------------------------------- | ---------------------------- |
| current gain    | $\beta$                                                                          | $\beta$                      |
| voltage gain    | $\frac{-g_{m}R_{c}}{g_{m}R_{e} + 1}$ ≈$-\frac{R_{c}}{R_{e}}$ if $g_{m}R_{e}$ ≫ 1 | -$g_{m}R_{c}$                |
| input impedance | $r_{\pi} + (\beta + 1)R_{e}$                                                     | $r_{\pi}$                    |
|                 | $R_{c}$                                                                          | $R_{c}$                      |
next is a list of  a few more properties of a BJT amplifier
- $I_{e} = I_{b} + I_{c}$ or $I_{e} \approx I_{c}$ 
- $I_{c} = \beta I_{b}$
- $I_{c} = \alpha I_{e}$  
- $\alpha = \frac{\beta}{\beta + 1}$ 
- $I_{c} \approx I_{s} e^{\frac{V_{be}}{V_{t}}}$  
- $I_{s}$ = emitter saturation current 
- $V_{t}=$ thermal voltage
  
A common circuit that is used for a common emitter is a self biased common emitter with degeneration(with or without a bypass capacitor in parallel with the degeneration resistance)

![[self biased common emitter circuit.png]]
## Simplified version
circuit gain can be also represented as
$$-\frac{Rout}{Re}$$
note that I use Rout to describe RC. This is another way to approximate the gain from the circuit that is considering that there is a emitter resistance.

## Solving in a simplified way
	- find the voltage at the base of the BJT (just a voltage division)
	- the emitter should have a similar voltage at the base just one forward voltage lower so if the base voltage was 1.83 then voltage at the emitter should be 1.13(if forward voltage is .7v)
	- find the current that is in the emitter(Ohms law with emitter voltage and emitter resistance)
	- this current is approximately the same current that is in the collector. Use that idea to find the voltage at the collector(Ohms' law wite collector current and collector resistance) you do Vcc - collector voltage to find the acutal voltage going into the collector.

its smart to do sanity checks to make sure that what you calculated makes sense so here are somethings to check when calculating. 
- check base current. This can be done by finding the emitter current the base current should be approximately $\frac{I_{e}}{\beta}$  this current needs to be negligible in order for the assumption of Ic = Ie. check the current going into the second resistor of the voltage divider at the base and compare that voltage for the theoretical base current calculated with beta. if the base current is really small compared to the current going into the second resistor then you can reasonably conclude that the base current is negligible.
- check if the emitter voltage is reasonable. current should go down from the BJT to ground and that is the assumed direction due to BJT arrow and where ground is. Which means if you find that the voltage at the emitter is negative then there is something wrong. Typically this just means that the Transistor isn't on as a negative voltage at the emitter doesn't make sense in this case
- check the voltage at the collector, again, if the voltage is a negative value that doesn't make sense. it is true common emitters are inverting so you should expect a negative sign at the output but remember that the transistor is being supplied a voltage range of 0 to VCC so it doesn't make any sense to the amplifier would have a negative voltage. also logically you do Vcc -(Ic)(Rc) this tells use the voltage left after going through the resistor voltage drop. The sum of all the voltage drops should equal the max voltage of Vcc so it wouldn't make sense to get a negative here.
[^1]: https://en.wikipedia.org/wiki/Common_emitter
[^2]: https://www.electronics-tutorials.ws/amplifier/amp_2.html
