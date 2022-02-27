# Non-overlapping clock generator for micro scale energy harvesting applications in 28nm CMOS technology
## Content
* Abstract
* Circuit details
* Circuit diagrams
* Generated waveforms from simulations
## Abstract: 
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
## Circuit diagrams:
* ### Block diagram of proposed circuit:
  ![image](https://user-images.githubusercontent.com/100309086/155555117-c5e6e32a-4fc4-4d93-a2ff-bac7dd750e4f.png)
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
* ### Overall circuit implementation :
  ![image](https://user-images.githubusercontent.com/100309086/155733402-75f7ff56-75e5-4b5f-a169-11800b969fa5.png)
* ### Analog IP of non overlapping clock generator :
  ![image](https://user-images.githubusercontent.com/100309086/155734783-34c462d8-156e-4f23-88e2-21600be7192f.png)
## Generated waveforms from simulations :
* ### Simulation schematic :
  ![image](https://user-images.githubusercontent.com/100309086/155734967-7399c6d6-6284-44b4-ac69-4ec4483001be.png)
* ### Simulation parameters :
  ![image](https://user-images.githubusercontent.com/100309086/155735206-33320cea-2e25-4d07-9801-1f6ed2275da6.png)
  ![image](https://user-images.githubusercontent.com/100309086/155735340-4fb7cf45-55d9-41f6-8a82-957bc453c498.png)
  ![image](https://user-images.githubusercontent.com/100309086/155735526-1aa25ae8-4ecc-4973-bf2b-028f293314bf.png)
  ![image](https://user-images.githubusercontent.com/100309086/155735635-827e80e2-35ba-47d0-a1f2-675ad9d786e6.png)
* ### Reference waveform :
  #### Non overlapping clock generator :
  ![image](https://user-images.githubusercontent.com/100309086/155736416-7364c13d-ee99-42b3-b280-61b43604eb81.png)
* ### Generated waveform :
  #### Current starved voltage controlled oscillator :
  ![image](https://user-images.githubusercontent.com/100309086/155869407-267dbccb-53a0-4b51-b637-9f5928f6d137.png)
  ![image](https://user-images.githubusercontent.com/100309086/155869375-2a6375f0-a076-423a-9335-5da80cda4989.png)
  #### Non overlapping clock generator :
  ![image](https://user-images.githubusercontent.com/100309086/155736768-6e499039-8efc-4457-a5bf-8f51920fe7dd.png)
  ![image](https://user-images.githubusercontent.com/100309086/155736931-01600b33-b6b2-41c6-8fd2-2eafa261d381.png)
* ### Area estimate :
  ![image](https://user-images.githubusercontent.com/100309086/155843234-4e815019-5d70-44d3-ae29-d526f0ed0c2d.png)
* ### Voltage-frequency characteristics :
  ![image](https://user-images.githubusercontent.com/100309086/155866883-5f272a01-a99f-4d04-a57d-79be93d8c2b2.png)
* ### Netlist :
 ```
 *  Generated for: PrimeSim
*  Design library name: vin_lib
*  Design cell name: nov_clk_gen_tb
*  Design view name: schematic
.lib 'saed32nm.lib' TT

*Custom Compiler Version S-2021.09
*Sat Feb 26 10:51:58 2022

.global gnd!
********************************************************************************
* Library          : vin_lib
* Cell             : cs_vco_1
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt cs_vco_1 gnd_1 vdd vctr vo_vco
xm10 vo_vco net68 net41 vdd p105 w=0.2u l=0.03u nf=2 m=1
xm9 net68 net64 net37 vdd p105 w=0.2u l=0.03u nf=2 m=1
xm8 net64 net60 net33 vdd p105 w=0.2u l=0.03u nf=2 m=1
xm7 net60 net56 net29 vdd p105 w=0.2u l=0.03u nf=2 m=1
xm6 net56 net65 net25 vdd p105 w=0.2u l=0.03u nf=2 m=1
xm5 net41 net92 vdd vdd p105 w=0.2u l=0.03u nf=2 m=1
xm4 net37 net92 vdd vdd p105 w=0.2u l=0.03u nf=2 m=1
xm3 net33 net92 vdd vdd p105 w=0.2u l=0.03u nf=2 m=1
xm2 net29 net92 vdd vdd p105 w=0.2u l=0.03u nf=2 m=1
xm1 net25 net92 vdd vdd p105 w=0.2u l=0.03u nf=2 m=1
xm0 net92 net92 vdd vdd p105 w=0.2u l=0.03u nf=2 m=1
xm21 net85 vctr gnd_1 gnd_1 n105 w=0.1u l=0.03u nf=1 m=1
xm20 net81 vctr gnd_1 gnd_1 n105 w=0.1u l=0.03u nf=1 m=1
xm19 net77 vctr gnd_1 gnd_1 n105 w=0.1u l=0.03u nf=1 m=1
xm18 net73 vctr gnd_1 gnd_1 n105 w=0.1u l=0.03u nf=1 m=1
xm17 net69 vctr gnd_1 gnd_1 n105 w=0.1u l=0.03u nf=1 m=1
xm16 vo_vco net68 net85 gnd_1 n105 w=0.1u l=0.03u nf=1 m=1
xm15 net68 net64 net81 gnd_1 n105 w=0.1u l=0.03u nf=1 m=1
xm14 net64 net60 net77 gnd_1 n105 w=0.1u l=0.03u nf=1 m=1
xm13 net60 net56 net73 gnd_1 n105 w=0.1u l=0.03u nf=1 m=1
xm12 net56 net65 net69 gnd_1 n105 w=0.1u l=0.03u nf=1 m=1
xm11 net92 vctr gnd_1 gnd_1 n105 w=0.1u l=0.03u nf=1 m=1
v27 net65 vo_vco dc=0 pwl ( 0 0.0 '1ns' 1 1.1n 1.2 1.2n 0.0 td=0 )
.ends cs_vco_1

********************************************************************************
* Library          : vin_lib
* Cell             : vin_inv
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt vin_inv gnd_1 in_inv out_inv vdd
xm0 out_inv in_inv gnd_1 gnd_1 n105 w=0.1u l=30n nf=1 m=1
xm1 out_inv in_inv vdd vdd p105 w=0.2u l=30n nf=2 m=1
.ends vin_inv

********************************************************************************
* Library          : vin_lib
* Cell             : D_ff
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt d_ff d gnd_1 q q_bar vdd clk_ff
xm1 net50 net52 net31 gnd_1 n105 w=0.1u l=0.03u nf=1 m=1
xm0 net48 clk_ff d gnd_1 n105 w=0.1u l=0.03u nf=1 m=1
xm3 net50 clk_ff net31 vdd p105 w=0.2u l=0.03u nf=2 m=1
xm2 net48 net52 d vdd p105 w=0.2u l=0.03u nf=2 m=1
c16 net50 gnd_1 c=0.05f
c15 net48 gnd_1 c=0.05f
xi13 gnd_1 q_bar q vdd vin_inv
xi12 gnd_1 net50 q_bar vdd vin_inv
xi11 gnd_1 net34 net31 vdd vin_inv
xi10 gnd_1 net48 net34 vdd vin_inv
xi14 gnd_1 clk_ff net52 vdd vin_inv
.ends d_ff

********************************************************************************
* Library          : vin_lib
* Cell             : clk_synch
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt clk_synch gnd_1 in_synch vdd phi phi_bar
xm0 net21 vdd in_synch gnd_1 n105 w=0.1u l=0.03u nf=1 m=1
xm1 net21 gnd_1 in_synch vdd p105 w=0.2u l=0.03u nf=2 m=1
xi4 gnd_1 net21 phi_bar vdd vin_inv
xi3 gnd_1 net16 phi vdd vin_inv
xi2 gnd_1 in_synch net16 vdd vin_inv
.ends clk_synch

********************************************************************************
* Library          : vin_lib
* Cell             : nov_clk_gen
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
.subckt nov_clk_gen gnd_1 vdd vctr phi phi_bar
xi0 gnd_1 vdd vctr net8 cs_vco_1
xi2 gnd_1 net12 net18 vdd vin_inv
xi1 gnd_1 net8 net12 vdd vin_inv
xi3 net54 gnd_1 net52 net54 vdd net18 d_ff
xi4 gnd_1 net52 vdd phi phi_bar clk_synch
.ends nov_clk_gen

********************************************************************************
* Library          : vin_lib
* Cell             : nov_clk_gen_tb
* View             : schematic
* View Search List : hspice hspiceD schematic spice veriloga
* View Stop List   : hspice hspiceD
********************************************************************************
xi0 gnd! net34 net8 phi phi_bar nov_clk_gen
v6 net8 gnd! dc=0.4
v1 net34 gnd! dc=1.2
c5 net33 gnd! c=0.05f
c4 net25 gnd! c=0.05f
xi10 gnd! net36 net33 net34 vin_inv
xi9 gnd! phi_bar net36 net34 vin_inv
xi8 gnd! net28 net25 net34 vin_inv
xi7 gnd! phi net28 net34 vin_inv








.tran '0.1n' '10n' name=tran

.option primesim_remove_probe_prefix = 0
.probe v(*) i(*) level=1
.probe tran v(phi) v(phi_bar)

.temp 25



.option primesim_output=wdf


.option parhier = LOCAL






.end
```
## Conclusion :
* A non overlapping clock generator for micro scale energy harvesting systems has been presented in this work.
* The results have been verfified with help of simulations using synopsys custom compiler in 28nm CMOS technology.
* It is suitable for micro scale energy harvesters generating electrical singnals in range of 0.3 to 0.4 volts.
## Author :
Vinod Kumar Yadav, Dept of Electronics Engineering, Govt Girls Polytechnic Gorakhpur.
## Acknowledgement :
1. Synopsys Company
2. IIT Hyderabad
3. VLSI System Design (VSD) Corp. Pvt. Ltd. India
4. Cloud based Analog IC Design hackathon, IIT Hyderabad
5. Kunal Ghosh, Co-founder, VSD Corp. Pvt. Ltd. India
6. Chinmaya Panda IIT Hyderabad
## References :
* [1] S. Mondal and R. Paily, “Efficient solar power management system for self-powered IoT node,” IEEE Trans. Circuits Syst. I Regul. Pap., vol. 64, no. 9, pp. 2359–2369, 2017, doi:10.1109/TCSI.2017.2707566.
* [2] M. S. Alam, M. Muqeem, and M. Hasan, “Ultra-low power clock generator for self powered IoT sensor nodes,” in Proceedings - 2019 International Conference on Electrical, Electronics and Computer Engineering, UPCON 2019, 2019, pp. 1–5, doi:10.1109/UPCON47278.2019.8980091.

  


