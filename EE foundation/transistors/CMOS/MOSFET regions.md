## Triode region (ohmic region)
![[Triode region.png]]
The triode region is a linear portion of a transistor where the current($I_{d}$) increases linearly with respect to the voltage from the drain with respect to the source($V_{ds}$). Obviously, by looking at the picture where the triode region lies, the curve isn't actually linear.  the linearity of the triode region is more of an approximation to represent this region without having to use complex equations to more accurately predict the MOSFET behavior. 

The other name of this region is ohmic region this name takes into account the "Linear" nature of this region. using [[Ohm's Law]], we can see the linear behavior of the current and voltage in this region means that we can see this MOSFET as a variable resistor
![[MOSFET as variable resistor.png]]
The criteria to be in this region is what is seen below
$$V_{ds} << 2(V_{gs} - V{th})$$


## Saturation
saturation is when $$V_{ds} > v_{gs} - V_{th}$$
looking at the picture of the region below you can see that $I_{d}$ remains relatively constant as $V_{ds}$ . So in this respect, the MOSFET can sorta resembled a current source as the $V_{ds}$ increase doesn't impact the current $i_{d}$ as it stays rather constant despite changes in voltages.
![[MOSFET saturation region.png]]
Some people may refer to a minimum voltage to stay in saturation region and they denote it like this.
$$V_{ds,sat} = V_{gs} - v_{th}$$
This is the bare minimum voltage to remain in the saturation region

## Cutoff
This is the "OFF" region of a MOSFET where the "electrical connection" between the source and the drain are not connected. Basically the region when the source and the drain are isolated from each other so flow of current cannot go between them. This occurs with the equation below
$$V_{gs} < v_{th}$$


## visualization of all regions
![[Mosfet regions visualization.png]]
