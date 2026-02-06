## time domain 
components like capacitors and inductors behave differently with respect to time. with this in mind that means that a capacitors behaviors different with time. for example, if you charge and discharge a capacitor the voltage at the capacitor changes with respect to time as the voltage rises(charging) or falls(discharges). This idea is the key principle for transient response of circuits in the time domain.

## equations
to map the charge time of a capacitor starting from $0V$ to $V_{max}$ you use the equation below
$$V_{cap} = V_{max}(1-e^{-\frac{t}{\tau}})$$
- $V_{max}$ = voltage supplied to the capacitor
- t = time
- $\tau$ = time constant 

to find the peak-to-peak voltages for a capacitor charging centered at a dc offset(typically happens when period of the square wave is less than 5$\tau$) you can use this equation below
$$V_{pp} = V_{max}*\frac{1-e^{-\frac{t}{2\tau}}}{1+e^{-\frac{t}{2\tau}}}$$
note that $2\tau$ isn't 2 time constants its actually $\frac{t}{2}*\frac{1}{\tau}$ it basically is finding the half period. This works for duty cycles of 50%

## time constant ($\tau$)
time constant is a metric that is used to describe how fast the capacitor will charge and is dependent on the **Resistance** and **Capacitance** of the circuit. The unit of this is seconds(hence the name time constant)
$$\tau = RC$$
so for example take this RC circuit 
![[RC circuit time constant.png]]
we can calculate the time constant of this circuit by doing
$$\tau = (1k)(1u) = .001s$$ this means that it will take .001s or 1ms for the capacitor to charge from 0 to 63.2% of $V_{max}$ just for clarification you can find this percentage from the $1-e^\frac{t}{\tau}$ section of the equation as that will give you a percentage. we know that 63.2% is when one time constant has passed that means $t =\tau$
and we get
$$V_{cap} = V_{max}(1-e^-\frac{\tau}{\tau})$$
which gives 
$$V_{cap} = V_{max}(.632)$$
with 2 time constants 
$$V_{cap} = V_{max}(1-e^-\frac{2\tau}{\tau})$$
$$V_{cap} = V_{max}(.864)$$
this can go on and on as the equation is asymptotic and will never actually hit $V_{max}$ so as a rule or thumb it is generally agreed that $4\tau$ or $5\tau$ is generally acceptable for the capacitor to be considered "fully charged" 
- $4\tau$ = 98.1%
- $5\tau$ = 99.3%

## Signal representation with time constants
generally you need 5 time constants for the signal to rise to a [[stead state todo ]] value and there are two changes in a period of a wave so generally speaking you would need $10\tau$ or greater for the period of the signal.
![[10time constant.png]]
green is the output of the capacitor and red is the signal with a period of $10\tau$ . as you can see in the graph the capacitor just barely reaches 5V(4.965V) then starts to discharge. This is where time constants become important. We allowed just enough time for the capacitor to charge to "5V" and discharge to "0V" if we reduced the period of the square wave( square wave period is less than $10\tau$) then the signal will never get to 5V or 0V when this happens the signal will start to become a triangle wave and slowly start to gain a dc offset and is charges and discharges
![[period = 1time constant.png]]
this picture demonstrates the triangle wave property and since the square wave is 50% duty cycle the triangle wave will be centered at Vmax/2 (if 25% then Vmax/4,etc) this is where you can use this equation to find the peak-to-peak values of the triangle wave
$$V_{pp} = V_{max}*\frac{1-e^-\frac{t}{2\tau}}{1+e^-\frac{t}{2\tau}}$$ we know the period of the square wave is 1Khz(period = .001s)and time constant is 1ms so we can plug both the period of the wave and the time constant to find the peak-to-peak value. I know that the triangle wave period if the same as time constant in this particular example but keep in mind that is how the example worked out. t = period of the signal and $\tau$ = time constant(RC).
$$\frac{.001}{2*.001} = .5$$
so 
$$V_{pp} = V_{max}*\frac{1-e^-.5}{1+e^-.5} = 1.22V$$
then you can find the peaks by doing
$$V_{peak} = \frac{1.22}{2} + 2.5 = 3.11V$$ and 
$$V_{trough} =2.5 - \frac{1.22}{2} = 1.88V $$

