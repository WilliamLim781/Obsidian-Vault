## what is a LUT
a Look Up Table (also known as a LUT) is a method in an FPGA, to store combinational logic. Instead of having combinational logic, a LUT can be used to store the logic of said circuit and output the desired output when the proper combinational logic is presented at the input.

## example
looking at a AND gate we have

| X   | Y   | OUT |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 0   |
| 1   | 0   | 0   |
| 1   | 1   | 1   |

this data is stored into the LUT that would take two inputs (x and y) and a output that corresponds to OUT on the table.  

## Why use it?
Traditionally you would need a 2 input AND gate to have this behavior
![[AND GATE.png]]
This works for specific circuit where all you will ever need is an AND gate. But what if you needed something more flexible or you don't know that you specifically need an AND gate. Having a [[black box]] circuit that can behave like any kind of combinational logic would be more convenient. That is what a LUT is. A [[black box]] that allow you to give it input and it will output based on the combinational logic you want it to.
![[LUT.png]]
