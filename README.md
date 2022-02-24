# Non-overlapping clock generator for micro scale energy harvesting applications in 28nm CMOS technology
### Abstract: 
* This report presents a non overlapping clock generator for micro scale energy harvesting applications. 
* The clock generator employs a current starved voltage controlled oscillator, D flip flop and clock synchronizer circuit.
* The current starved voltage controlled oscillator has been realized using CMOS ring oscillators.
* The proposed circuit has been simulated using synopsys custom compiler in 28nm CMOS technology.
## Circuit details:
* Non overlapping clock generator is an important part of control circuitry employed for maximum power point tracking in micro scale energy harvesting systems.
* Non overlapping clocks prevent the reverse flow of current in charge pump based DC-DC boost converter.
* Authors in [1] have presented non overlapping clock generator realized using CS-VCO and phase shifters.
* D-flip flops have been employed to generate clocks with 50% duty cycle but the proposed design is not optimum in terms of area due to consisting large number of transistors.
* Authors in [2] have proposed the non-overlapping clock generator realized using concept of dynamic threshold MOSFET but the frequency variation is not possible in chip design due to fixed values of resistors and capacitors used in ring oscillator.
* In this work, a non- overlapping clock generator has been proposed which requires lesser number of transistors occupying lesser area along with a provision for variable frequency.
## Circuit design:
* ### Block diagram of proposed circuit:
  ![image](https://user-images.githubusercontent.com/100309086/155555117-c5e6e32a-4fc4-4d93-a2ff-bac7dd750e4f.png)
* ### Block diagram of implemented circuit:
  ![image](https://user-images.githubusercontent.com/100309086/155552694-2fddab46-c11a-4a46-b95b-d716b28ece08.png)
* ### Proposed circuit for current starved voltage controlled oscillator (CS VCO):
  ![image](https://user-images.githubusercontent.com/100309086/155554918-6afbb35c-ff23-43e6-a0a6-6d62aced9d97.png)
* ### Implemented circuit for CS-VCO:
  ![image](https://user-images.githubusercontent.com/100309086/155555654-37456029-d4cb-4dc7-a697-926a06b583fd.png)
* ### Implementation of inverter circuit:
  ![image](https://user-images.githubusercontent.com/100309086/155556610-cd02dc73-bfd1-4029-8ca8-13ec4bb26038.png)
* ### Proposed circuit for D flip flop:
  ![image](https://user-images.githubusercontent.com/100309086/155557050-8b6d8e0e-4dc4-4ca6-a63f-cf38e8ba4f04.png)
* ### Implemented circuit for D flip flop :
  ![image](https://user-images.githubusercontent.com/100309086/155557493-173d498a-da45-4bde-86ea-40538c608c8e.png)
* ### Proposed circuit for clock synchronizer :
  ![image](https://user-images.githubusercontent.com/100309086/155557929-8f1a1966-a189-4266-903c-f261f60fb5f7.png)
* ### Implemented circuit for clock synchronizer :
  ![image](https://user-images.githubusercontent.com/100309086/155558194-5d4f8d0b-811a-446d-a0fd-226c16d47ee3.png)


