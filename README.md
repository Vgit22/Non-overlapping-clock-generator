# Non-overlapping clock generator for micro scale energy harvesting applications in 28nm CMOS technology
### Abstract: 
* This report presents a non overlapping clock generator for micro scale energy harvesting applications. 
* The clock generator employs a current starved voltage controlled oscillator, D flip flop and clock synchronizer circuit.
* The current starved voltage controlled oscillator has been realized using CMOS ring oscillators.
* The proposed circuit has been simulated using synopsys custom compiler in 28nm CMOS technology.
## Introduction:
* Non overlapping clock generator is an important part of control circuitry employed for maximum power point tracking in micro scale energy harvesting systems.
* Non overlapping clocks prevent the reverse flow of current in charge pump based DC-DC boost converter.
* Authors in [1] have presented non overlapping clock generator realized using CS-VCO and phase shifters.
* D-flip flops have been employed to generate clocks with 50% duty cycle but the proposed design is not optimum in terms of area due to consisting large number of transistors.
* Authors in [2] have proposed the non-overlapping clock generator realized using concept of dynamic threshold MOSFET but the frequency variation is not possible in chip design due to fixed values of resistors and capacitors used in ring oscillator.
* In this work, a non- overlapping clock generator has been proposed which requires lesser number of transistors occupying lesser area along with a provision for variable frequency.
