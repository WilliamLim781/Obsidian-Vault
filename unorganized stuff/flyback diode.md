a flyback diode (also known as a freewheeling diode) is a diode that is connected across an inductor to remove/eliminate flyback. Flyback is when there is a voltage spike that is seen across the inductive load. Flyback occurs the source that is supplying power to the inductor is removed and the inductor behaves like a source. Flyback diodes can be seen in any circuit that includes an indcutor. For example that this simple DC motor circuit and look at the diode that is connected in parallel with the motor.
![[Flyback diode on dc motor.png]]
In the picture you can see that a diode is connected to a motor. Motors counts as inductors since they are essentially long spools of wires. Notice that the diode is wired so that it is reversed biased to the 5v so it doesn't conduct when you have the 5V powered in the motor. When the 5v is removed then the motor becomes the source of power and all that power will flow through the diode and back into the motor. Basically the diode becomes a short with the inductor and allows it to remove the energy is build up safely.



https://en.wikipedia.org/wiki/Flyback_diode