Operational amplifier (op-amp) is a DC-coupled voltage amplifier. it contains a [[differential input]](V+ and V-) and one output(Vout). Op-amps tend to have very high [[gain(TODO)]]. To manage gain a negative feedback in op-amps you can control gain with external components to make the gain more manageable and designable.
## fundamental equation
$$V_{out} = A_{o}(v_{+} -V_{-})$$
where $V_{out}$ is the output of the op-amp and $V_{+}$ and $V_{-}$ are the inputs. $A_{o}$ is known as open gain and in theory it is very large but in reality  you can find really high values like 400 (typical value for the op07).
![[Op-amp picture.png]]
## common topologies
list is from:https://www.arrow.com/en/research-and-events/articles/fundamentals-of-op-amp-circuits
- [[voltage follower]]
- [[Inverting Op-amp]]
- [[Non-inverting Op-amp]]
- [[Non-inverting summing amplifier(TODO)]]
- [[Inverting summing amplifier]]
- [[Differential amplifier(TODO)]]
- [[Integrator(still needs a simulation)]]
- [[Op-amp differentiator(TODO)]]
- [[Converter current - voltage (TODO)]]
- [[negative resistance(TODO)]]
For an ideal op-amp there are a few characteristics to remember

| characteristic         | value    |
| ---------------------- | -------- |
| open-loop gain(A)      | infinite |
| input resistance       | infinite |
| output resistance      | 0        |
| bandwidth of operation | infinite |
| dc bias offset         | 0        |

![[ideal opamp.png]]
there are two  concepts that you need 
1. the current I1 and I2 are zero
2. the voltage at V1 and V2 are the same
[^1]: https://www.electrical4u.com/ideal-op-amp/
	
