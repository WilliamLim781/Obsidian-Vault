## Truth table

| B   | A   | Z   |
| --- | --- | --- |
| 0   | 0   | 0   |
| 0   | 1   | 0   |
| 1   | 0   | 0   |
| 1   | 1   | 1   |

## Symbol
![[AND gate symbol.png]]

## Transistor form
The transistor form of an AND gate just comprises of a series NMOS connected to 5V and a parallel. A little tip for knowing what is in series and what is in parallel is based on the truth table. Since we know that then A = 1 and B = 1 that mean that they both have to be on for $V_{dd}$ to be read. That means that there needs to be  **TWO** NMOS transistor in series under the $V_{dd}$ line. NMOS because logic is read as 1 = gate open and 0 = gate closed. When you have the same output but the inputs can vary that means you have parallel NMOS or PMOS. The use NMOS or PMOS is dependent on what  the output is when you have both outputs on or off. Using the AND gate as an example tells you that if **A** and **B** are off then the output is 0 which means parallel PMOS at ground.
![[AND Gate sim.png]]


output

![[AND gate sim timing diagram.png]]

