## Truth table

| B   | A   | Z   |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 1   |
| 1   | 0   | 1   |
| 1   | 1   | 1   |

## Symbol
![[OR gate symbol.png]]

## transistor form
Unlike the [[AND]] gate there is a parallel NMOS on the top. This is due to the truth table having multiple combinations of **A** and **B** that will lead to the same output of $Z = V_{dd}$ Since we have the value of Z = 1 when A = 1 and B = 1  will mean that you need an NMOS to achieve this criteria. The bottom is filled with a series PMOS to ground which correlates with the idea when A = 0 and B = 0 then Z = 0.
 ![[OR Gate sim.png]] 

![[OR gate sim timing diagram.png]]