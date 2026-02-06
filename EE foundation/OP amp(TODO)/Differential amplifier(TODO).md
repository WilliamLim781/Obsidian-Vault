![[Differential amplifier op amp.png]]
A differential amplifier is a voltage subtractor. It basically takes in two different signals and subtracts and amplifies the said difference between the two different signals. The equations can get rather messy but the op amp is solved just like any other op amp equations. you just need to remember the two properties of an op amp(1.$v_{+} = V_{-}$ and 2.)current going into the op amp is zero). Note that since you have a signal going into both the positive and negative terminal the first property becomes rather important.

![[differential amplifier op amp equations.png]]
Notice that if $V_{2}$ is zero then the op amp basically behaves as a inverting amplifier which makes sense as if $V_{2}$ is zero it basically serves as ground and the resistors in the negative terminal don't really do anything as there is zero voltage there. So, the op amp basically turns into a inverting amplifier topology.
![[differential amplifier op amp vout.png]]
to make the equation more straight forward you can make $R_{1} = R_{2}$  and $R_{3} = R_{4}$ to make the the $V_{out}$ equations more simpler and make the equation represent more of a subtractor as the name of the op amp suggests
![[differential amplifier simulation.png]]

using the more simplified equation for a differential amplifier we get a value of 5v(used DC sources to make the subtraction properties more easier to see). if we plug in the values from the simulation into the equation we get

$$\frac{5k}{1k} (3-2) = 5V$$ which supports the simulation