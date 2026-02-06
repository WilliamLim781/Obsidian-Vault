RC filters are filters that use both a resistor and capacitor either in a series or parallel manner([[Equivalent Resistance]]) to filter out frequencies. Typically a RC filter in series is used for filtering high frequencies also known as a [[low pass filter(TODO)]]. 

## properties for first order RC filter


| characteristic   |                                               |
| ---------------- | --------------------------------------------- |
| pass band        | 0 dB                                          |
| Stop band        | -20 dB per octave                             |
| corner Frequency | -3 dB or .707Vin  and $45\degree$ phase shift |
| attenuation      | -20db per decade after cutoff freqeuncy       |
## corner frequency
To equation to find the corner frequency is given below
$$f_{c} = \frac{1}{2\pi RC} $$
where R is the resistance in $\Omega$ and C is the capacitance in farads. Note that you $\omega = 2\pi f$ so you can rearrange the question to get angular frequency as well 
$$\omega_{c} = \frac{1}{RC} $$
now moving onto a simulation of the RC filter. plugging in the values into the equation we get a $f_{c} = 1.59Khz$ so at 1.59Khz we should expect to be a -3db attenuation and a $45\degree$ phase shift.
![[RC low pass LTspice.png]] 
looking at the simulation we can confirm that there is indeed a 3dB attenuation at the calculated corner frequency and there is also a $45\degree$ phase shift as well at the corner frequency. 
![[RC low pass filter Sim.png]]
another property is that attenuation is -20dB for every decade after the corner frequency. Which means if you had a corner frequency of 1.59khz then for every move of the decimal point to the right of the corner frequency(i.e 15.9khz) you will have 20dB of attenuation. Looking at the attenuation of at 15.9khz at the simulation supports this idea
![[RC filter -20db.png]]
When chaining multiple RC filters you increase the order of the low pass filter (1 RC network is first order 2 RC network is 2nd order etc.) this effectively makes the corner frequency have more attenuation and slope of attenuation more sharp. for a first order filter, you have -20dB attenuation every decade, for a 2nd order you have -40db, 3rd order you have -60dB etc. The attenuation at the corner frequency isn't as simple from simulation I got. 1st order is -3db, 2nd order is -9db, and 3rd is -16db. Note that if you take a differential output from the resistor you will get a high pass filter with the same cutoff frequency