# CMOS-DESIGN- 

# 🚀 CMOS DESIGN LAB

Welcome to the **CMOS Design and Simulation Repository**.

This repository documents a **day-wise learning journey of CMOS design**, covering MOSFET physics, CMOS inverter behavior, SPICE simulations, switching analysis, noise margins, and process variations using SKY130 technology.

---

# 📚 Course Navigation (Click to Open)

> Select any day below to directly open the detailed notes and simulations.

| Day | Topic | Open |
|-----|------|------|
| **Day 1** | NMOS Id–Vds, Device Physics & Operation | 👉 [Open Day 1](./Day%201/README.md) |
| **Day 2** | Velocity Saturation & CMOS Voltage Transfer Characteristics | 👉 [Open Day 2](./Day%202/README.md) |
| **Day 3** | Switching Threshold & Dynamic CMOS Simulation | 👉 [Open Day 3](./Day%203/README.md) |
| **Day 4** | CMOS Noise Margin Analysis | 👉 [Open Day 4](./Day%204/README.md) |
| **Day 5** | Power Supply & Process Variation Analysis | 👉 [Open Day 5](./Day%205/README.md) |

---

# 🧠 Topics Covered

## 🔹 MOSFET Fundamentals
- NMOS structure and operation
- Threshold voltage physics
- Body effect
- Drift current derivation
- Regions of operation
- Pinch-off condition
- Channel length modulation

## 🔹 CMOS Inverter Theory
- Voltage Transfer Characteristics (VTC)
- Switching threshold analysis
- Region identification
- PMOS vs NMOS strength ratio

## 🔹 Short Channel Effects
- Velocity saturation
- Long vs short channel comparison
- Transconductance behavior

## 🔹 Timing Analysis
- Rise and fall delay
- Load capacitance effects
- Buffer sizing
- Clock inverter characteristics

## 🔹 Noise & Robustness
- Noise margins (NMH, NML)
- Safe vs unsafe glitches
- Static robustness evaluation

## 🔹 Process & Supply Variations
- Oxide thickness variation
- Etching variation
- Device mismatch
- Power supply scaling effects

---

# 🛠 Tools & Technologies Used

- **NGSPICE**
- **SKY130 PDK**
- CMOS Device Physics
- Analog & Digital Circuit Theory
- SPICE Netlist Simulation

---

# 📂 Repository Structure

Day 1/README.md
 NMOS Id vs Vds

CIRCUIT DESIGN AND SIMULATION      
CIRCUIT DESIGN 

Logic Gates, Inverters, Buffers ARE MADE FROM PMOS/NMOS AND Connected TO perform functions.

<img width="253" height="361" alt="image" src="https://github.com/user-attachments/assets/b1859f74-8a66-4f84-847c-b30277e69943" />
<img width="243" height="181" alt="image" src="https://github.com/user-attachments/assets/a0eab289-de48-4c5b-80b0-a1659098edc3" />
<img width="596" height="357" alt="image" src="https://github.com/user-attachments/assets/73be0698-285b-4a8c-9c4b-bda0374d375d" />

Delay in inverter is fetched by voltage transfer characteristics  of nmos or pmos .

The current id is directly propotional to W/L ratio ,then  Current decides the delay of the circuit.

Consider the example – functionality of Clock tree synthesis on the buffer circuit – Drive the different capacitive load at the output 

To change delay change w/l in simulation .

<img width="636" height="221" alt="image" src="https://github.com/user-attachments/assets/d56b420a-d2f1-45e3-87d6-311a1e708c03" />

<img width="326" height="375" alt="image" src="https://github.com/user-attachments/assets/d3ef9605-0d6a-47c3-9ddd-89e6f82a3816" />
<img width="306" height="369" alt="image" src="https://github.com/user-attachments/assets/fb352b3d-03f6-4e8f-85fd-952612255aee" />
Different W/L ratios produce different delay tables. Each delay value is obtained from the common point or the intersection of a same row and column which results in to the input slew rate and output capacitive load. If an exact pair of values is not available in the table interpolation is used to take the nearest delay value.

NMOS

<img width="338" height="159" alt="image" src="https://github.com/user-attachments/assets/6d93ecf1-c96c-409a-a1ba-166dbc080797" />
This is p substrare on which the device will be formed , all the regions will be defined on it

<img width="332" height="126" alt="image" src="https://github.com/user-attachments/assets/e525c16c-75f2-428d-9844-9f1ce43902be" />
There is an isolation area that will separate the device from being shot and define functionality 

<img width="343" height="183" alt="image" src="https://github.com/user-attachments/assets/371b7118-d791-42c5-a95d-160b9a5f43d2" />

N+ and n + region are doped regions where source and drain are defined , these regions are there to create the channel so that electrons may flow easily to conduct. 

<img width="339" height="187" alt="image" src="https://github.com/user-attachments/assets/633d4d03-25d7-426e-83c6-6d296b6d71c7" />

There is an oxide layer , sio2 , above this layer there is a metal connect that is called gate , that gate defines the charge carriers that will flow from the channel. More vg more elelctrons more current. 

<img width="339" height="181" alt="image" src="https://github.com/user-attachments/assets/5d9860bb-7120-4f00-a74e-9406a340ce63" />

As we discussed above there is a gate that controls the charge carriers and define the conductivity , this layer is created through the technique called metal deposition or ald atomic layer deposition

<img width="338" height="169" alt="image" src="https://github.com/user-attachments/assets/a6b45865-ad72-494a-b406-15fae1df6fcf" />

This is p substrate that is mostly shorted , but if used as potential it can effect vth 

Threshold voltage is the minimum voltage that has to be overcome to generate charges and flow of electron
Threshold voltage Equation 

<img width="936" height="254" alt="image" src="https://github.com/user-attachments/assets/88fae22f-1cee-4c3d-8112-ff03f4b896fa" />

Channel b/w source and drain has  very high resistance no conductivity  between source & drain.
To conduct 
Provide vgs positive , that will attract the electrons from the p substrate to create the channel of electrons , so that electrons from source passes through channel to drain and to ground so that there is an current id from drain to source. This is how conductivity came into system. 

<img width="651" height="370" alt="image" src="https://github.com/user-attachments/assets/64cbbeb7-3332-4cf2-9b1c-d2c4149ebd51" />

This we have discussed that how the accumulation of negative charge is there and forms channel. 

When +VGS is given  accumulation of negative ions in the depletion region under the gate  depletion region is formed under the source and drain region 
More +VGS width of depletion area increase  at one value of VGS, surface near the Gate Oxide is inverted that is  surface inversion or strong no this is no more p type it is n type.

<img width="508" height="258" alt="image" src="https://github.com/user-attachments/assets/c8a40821-369a-4447-b8e9-f0c3b5393818" />

<img width="360" height="313" alt="image" src="https://github.com/user-attachments/assets/213d38cb-e977-4453-aec9-2a0fccba274d" />
More vgs more electron less resistance now current can flow.

<img width="384" height="222" alt="image" src="https://github.com/user-attachments/assets/6287b416-b78a-4aca-a755-8a9b11e9f317" />

Effect of Body terminal on threshold 
If VSB is positive there will be reverse bias between source and substrate due to which  wider depletion region near the source region than drain side increases

<img width="377" height="275" alt="image" src="https://github.com/user-attachments/assets/c1d395d6-55cc-437c-b3d8-01b19946d622" />

When +VGS is increases the width of depletion region increases in both cases it is that expected the accumulation of the negative charge carrier 

<img width="940" height="396" alt="image" src="https://github.com/user-attachments/assets/8b6e697d-67fe-4c63-8b14-7d2685889854" />

Vgs is trying to form the channel and vsb is disturbing it due to depletion width. 

<img width="716" height="302" alt="image" src="https://github.com/user-attachments/assets/48748abd-17b1-400f-b48e-2877c376476d" />

As  we can clearly see the depletion width near source is more due to body effect. 

<img width="463" height="177" alt="image" src="https://github.com/user-attachments/assets/6fc3f758-5761-4fe8-a8e8-23e4008916f6" />

Vt – threshold voltage , defined by foundary during the process 
γ – body effect , it shoes how substrate can hamper the vth.

<img width="879" height="263" alt="image" src="https://github.com/user-attachments/assets/8880b465-b97e-4eeb-81b0-057bbe886459" />

These are the parameters on which it is dependent, all defined by the foundary.

REGION OF OPERATION OF NMOS 
NMOS Transistor operates  in 3 regions 
 VGS < Vt   Cut-off region 
 VGS > Vt

<img width="668" height="411" alt="image" src="https://github.com/user-attachments/assets/6286f967-b5b1-43cc-90cf-788d172de833" />

First we have to apply the voltage vgs>vt , only then we can define region of operation if not then the tx is in cutoff region , non operation mode. Nothing is happening.
WHEN VDD IS APPLIED AND VDS ALSO COMES INTO PLAY . 

<img width="974" height="352" alt="image" src="https://github.com/user-attachments/assets/269ba89b-3970-498e-ba30-ef1ca69c7d6e" />

Voltage difference between the ends of the channel – one end connected to the source which is grounded – other end connected to Drain connected to +VE supply voltage 
Voltage across the channel in the presence of VDS is not constant – was constant when VDS was 0


DRIFT CURRENT 
Effective channel voltage at any point in the channel: VGS – V(X)
When X = 0 (source End) V(X) = 0
When X is considered at Drain end  V(X) = VDS

<img width="493" height="342" alt="image" src="https://github.com/user-attachments/assets/b1dc55ac-6cf3-4e66-ba38-6c492e248cdd" />

Effective channel voltage – Ranges from 1V to 0.95V – Gradient – goes from higher (source) to lower (drain) – 
 VGS > Vt  – create the equivalent amount of induced charge in the channel (When VDS = 0V)
When VDS is connected to supply and VGS > Vt, induced charge at any point in the channel  

<img width="940" height="509" alt="image" src="https://github.com/user-attachments/assets/c2623400-97f6-4c5b-9007-9ab4274ee4a6" />

Require to put value of velocity of charge, available charge – Integrate over whole channel width to have drain current value

Velocity of the charge carrier – not constant due to voltage gradient in the channel 
<img width="384" height="258" alt="image" src="https://github.com/user-attachments/assets/45df1f62-749c-4bca-bf2c-116acde129af" />
dV – change in the channel voltage – can go from 0 to VDS
dX – change in the channel – can go from 0 to L

<img width="386" height="121" alt="image" src="https://github.com/user-attachments/assets/3cd76d6e-ed0a-4d43-8523-d80b920126d2" />

Integrating over respective ranges in RHS and LHS
ID = µNCOXW/L(VGS – VT)2 FOR SATURATION 
I ID = µNCOXW/L((VGS – VT) – VDS2/2) FOR LINEAR REGION 
IF THERE IS ANY CHANNEL LENGTH MODULATION THEN THERE IS EXTRA TERM ADDED IN BOTH 1+ƛvds.
Equation – model of MOSFET - µn, Cox, W/L, kn’, kn – Constant - technological parameter – model parameter – require to pass to SPICE simulation to computer drain current
We can’t say that Id is in linear region as Id is quadratic function of Vds. 
Let us put the values in the derived equation
(Vds)2 is almost zero when Vds <= (Vgs-Vt) 
Condition for the linear region - Vds <= (Vgs-Vt)
As long as condition is satisfied – Id is said to be linear function of Vds – Small value of Vds generally satisfy this condition.

SPICE RESULT 
Requires to see the impact of Vgs and Vds on Id when both are varied – How the device behave when these two voltages are getting changed
Analyse effect of VGS and VDS on ID — use multiple voltage values — device stays in linear region when VDS < (VGS − Vt) — fix VGS — sweep VDS from 0 to (VGS − Vt) — compute ID using linear-region equation — verify ID–VDS curves with SPICE simulations

PINCH OFF 
on Channel voltage at drain-end: VGS – VDS
Channel voltage > Vt to form surface inversion – requirement to turn the device 

<img width="464" height="316" alt="image" src="https://github.com/user-attachments/assets/5b2fb522-3076-41de-bd38-f8f55e7431d7" />

Varying the VDS while keeping VGS and Vt constant – feed to SPICE simulator 
Important to understand when channel voltage (VGS – Vt) < Vt 
As long as channel voltage (VGS – Vt)  > Vt – valid conducting channel exist in between source and drain

<img width="589" height="286" alt="image" src="https://github.com/user-attachments/assets/975ac4f1-2b4d-4002-ab7b-abda3a6ab7cb" />

When channel voltage (VGS – Vt)  = Vt – two different scenario at source end and drain end –Surface inversion at source end has already happened as channel voltage at source end is higher than Vt – Surface inversion is just happened as channel voltage at Drain end is exactly at Vt – mix and max of two concepts -  channel will start disappear from the drain side – this phenomena is known as pinch-off situation   

<img width="609" height="302" alt="image" src="https://github.com/user-attachments/assets/a96b7eae-7380-4815-96a7-c8539aa864d2" />

<img width="352" height="352" alt="image" src="https://github.com/user-attachments/assets/ddfb5fd1-dbfc-4748-af03-0118a35539bb" />

On or After the pinch-off situation – further increase in VDS cause MOSFET to drive in saturation - current will not stop flowing – linearity will change 

<img width="678" height="333" alt="image" src="https://github.com/user-attachments/assets/84a5b413-f65a-432a-9216-4928e7c11cb0" />

Pinch-off situation – converted in model or current equation – feed the SPICE simulator   

DRAIN CURRENT MODEL 
On or After the pinch-off situation – further increase in VDS cause MOSFET to drive in saturation – voltage over the channel – constant – (VGS – Vt) – no dependency on VDS
Saturation region – channel voltage remains constant = (VGS – Vt) 
Linear region – channel voltage depends on VDS = (VGS – V(X))
Effective channel length is smaller than effective gate length 
Effective channel length – modulated by VDS

<img width="450" height="336" alt="image" src="https://github.com/user-attachments/assets/229cfaf5-8695-4e88-908c-1571b76edb91" />


Deriving the current equation in saturation region, we can have following equations from the drain current model for linear region of operation
 In linear region – Square of VDS – very near to 0 – Ignored
In saturation region – channel voltage – (VGS – Vt) – Replacing VDS by (VGS – Vt) 

<img width="378" height="382" alt="image" src="https://github.com/user-attachments/assets/032fecf8-29bd-464b-9608-6feb57fa7486" />

 Id is constant current all parameters are constant but has dependency on w and L has dependency VDS Accurate equation requires effect of VDS.
 

SPICE SIMULATION 

SPICE HAS pre defined models that are used to build circuits , these models have all the necessary parameters that are used for simulation of the circuit , we have to use thesde parameters as per our requirement , for static or transient analysis. 

<img width="733" height="328" alt="image" src="https://github.com/user-attachments/assets/d993e80f-ee02-4eaa-a088-75dfb9804964" />

these are the parameters that are defined for the simulation of the circuit, based on the tech 180nm or 130nm , we will use these parameters 

<img width="426" height="198" alt="image" src="https://github.com/user-attachments/assets/8976172d-4862-40c2-b354-7414c2adc960" />

resistor is applied so that gate may not damage from the high current or voltage 

TECHNOLOGY PARAMETER 







DAY 2/README.md


VELOCITY SATURATION 
CMOS INVERTER 
VTC VOLTAGE TRANSFER CHARACTERSTICS 

<img width="549" height="466" alt="image" src="https://github.com/user-attachments/assets/5eb8f2f8-9eb3-4e6b-97fc-42f100761043" />

UNDERSTANDING THIS GRAPH 
    cutoff region id = 0 , vgs < vt 
    
•	Linear Region is the Resistive Region where the graph seems linear , vgs > vt , vds < vgs - vt,  •	Id = µn cox w/l ((vgs – vt) – vds2/2))
    saturation region , the transition from linear to constant , vgs > vt , vds > vgs - vt , id = µn cox w/l (vgs - vt)^2/2

•	If W/L ratio is constant from 1200 nm (1.2 µm) to 250 nm (0.250 µm) for different technological node – Id in saturation current seems same irrespective of the technological node but the case is not the true for the lower node

ID VS VGS ( TRANSCONDUCTANCE ) DID/DVGS = GM , FOR LONG CHANNEL AND SHORT CHANNEL 

ID IS directly propotional to square of vgs - vt , that is why there is difference in the graph at different values of vgs ,
In short channel the velocity saturation is the driven factor for the id but at a specific voltage the velocity dont increase so the current also dont increase and the gm decreases that is bad for gain. good for digital design and bad for analog design. 

<img width="939" height="453" alt="image" src="https://github.com/user-attachments/assets/85463e5d-eb28-4a22-bb1c-32894f504a70" />

less than 250 nm is considered as short channel device
<img width="749" height="381" alt="image" src="https://github.com/user-attachments/assets/543b950b-7787-47a2-910a-4bfd60095c47" />

Id-Vgs with Vds = 1.8V – L = 1.2 µm (long channel) is more curved than L = 0.25 µm (short channel) – L = 0.25 µm is more linear than L = 1.2 µm – Comparison is done for same W/L. 

<img width="782" height="237" alt="image" src="https://github.com/user-attachments/assets/60ee906a-4750-4a2d-946a-41bceb27e477" />

VELOCITY SATURATION AT HIGH ELECTRIC FIELD 

<img width="437" height="306" alt="image" src="https://github.com/user-attachments/assets/a2437eea-1922-476c-af04-583d722f2e4e" />
<img width="405" height="288" alt="image" src="https://github.com/user-attachments/assets/73041a30-3753-4381-ab3e-575da156b522" />

Short channel – initial behaviour still follows the quadratic relation followed by linear region operation due to velocity saturation
Concept of velocity saturation – for lower values of electric field, it follows the linear behaviour but after some critical electric field Ɛc, it tends to constants 

<img width="940" height="410" alt="image" src="https://github.com/user-attachments/assets/5b59b695-3c6f-4d87-a56e-72594b36cd6d" />

THIS IS VERY COMPLEX , WE NEED A COMPACT MODEL A SIMPLE MODEL 

<img width="940" height="293" alt="image" src="https://github.com/user-attachments/assets/de8b92ef-8a6f-4194-9442-bbba8c0c3a9d" />

VELOCITY SATURATION IS 4th REGION OF SATURATION 

<img width="939" height="379" alt="image" src="https://github.com/user-attachments/assets/f6e375c2-1dcb-467d-bc87-2cc0ee9f84b0" />

ID VELOCITY SATURATION 

One drain equation represents all the regions by considering the minimum of Vgt, Vds and Vdsat. 
Earlier section, the effect of (1 + λVds) is considered in only saturation region but here it will be kept as for lower value of Vds, it will be vanished. 
Vdsat – voltage at which device velocity saturate – technological parameter – independent of Vgs and Vds – foundry parameter – open model file when the node is less than 250 nm to check the Vdsat value

<img width="515" height="186" alt="image" src="https://github.com/user-attachments/assets/8c505594-765e-4111-a1ac-804be0b89659" />

When Vgt is minimum, it implies that Vds and Vdsat is higher – device goes in saturation – applicable for bot short channel and long channel device
When Vds is minimum – lower values of Vds, the device will operate in resistive/linear region of operation – due to smaller value of Vds, the term (1 + λVds) will be ignored – applicable for both short and long channel device

<img width="527" height="101" alt="image" src="https://github.com/user-attachments/assets/4c305d19-64cc-4784-8f7c-23380e5b15bb" />

When Vdsat is minimum – device enter in velocity saturation – only in short channel device – when node is less than 250 nm 

<img width="532" height="99" alt="image" src="https://github.com/user-attachments/assets/502e8284-43e0-426a-b719-42b7f1e9c609" />

For short channel, peak saturation current is always lower than peak saturation current of long channel device – Compared on same W/L

<img width="940" height="406" alt="image" src="https://github.com/user-attachments/assets/0743f51e-11e7-4e13-83d6-10c972131a2d" />

<img width="398" height="108" alt="image" src="https://github.com/user-attachments/assets/5b43932b-c09d-40dd-8fe3-76aede644869" />

dsat is a technology parameter saturation voltage i.e voltage at which device velocity saturates and is independent of Vgs or Vds

The various modes when the value of Vmin is different

When Vgt is the minimum of Vgt, Vds, Vdsat the device is in saturation region.
When Vds is the minimum of Vgt, Vds, Vdsat the device is in resistive region.
When Vdsat is the minimum of Vgt, Vds, Vdsat the device is in velocity saturation region.
It looks like current should increase at lower nodes.
Velocity Saturation causes device to saturate early


LAB 

ID VS VDS 

*Model Description
.param temp=27

*Including sky130 library files
.lib "sky130_fd_pr/models/sky130.lib.spice" tt

*Netlist Description

XM1 Vdd n1 0 0 sky130_fd_pr__nfet_01v8 w=0.39 l=0.15
R1 n1 in 55

Vdd vdd 0 1.8V
Vin in 0 1.8V

*simulation commands

.op
.dc Vdd 0 1.8 0.1 Vin 0 1.8 0.2

.control

run
display
setplot dc1
.endc

.end

<img width="1920" height="1031" alt="image" src="https://github.com/user-attachments/assets/dffce14b-def6-4dcc-9d27-7ea2fe321085" />

To observe the value of Id at any point on the curve, then left click on the point on the curve to be observed.
Now on the terminal window, some values of x0 and y0 should appear.
The value of Id corresponds to the value of y0 in ampere

VTH FOR ID VS VGS 

*Model Description
.param temp=27

*Including sky130 library files
.lib "sky130_fd_pr/models/sky130.lib.spice" tt

*Netlist Description
XM1 Vdd n1 0 0 sky130_fd_pr__nfet_01v8 w=0.39 l=0.15
R1 n1 in 55

Vdd vdd 0 1.8V
Vin in 0 1.8V

*simulation commands

.op
.dc Vin 0 1.8 0.1

.control

run
display
setplot dc1
.endc

.end

<img width="1920" height="1028" alt="image" src="https://github.com/user-attachments/assets/73dd7b16-d711-4ff6-b695-0a7803729b7b" />

the linear part of the plot must be extended. Now, the x intercept of this extended plot gives the value of the threshold voltage of the device that is being simulated


CMOS VTC VOLTAGE TRANSFER CHARACTERISTICS 

The working of CMOS inverter

What happens when Vin is ‘high’ and equal to ‘vdd’

PMOS turns 'OFF'
NMOS turns 'ON'
What happens when Vin is ‘low’ and equal to ‘0V’

PMOS turns 'ON'
NMOS turns 'OFF'
The flow of current when Vin is ‘high’ and when Vin is ‘low’

When Vin=Vdd

Direct path exists between Vout and Vss resulting in Vout=0V
When Vin=0V

Direct path exists between Vdd and Vout, resulting in Vout=Vdd


<img width="390" height="368" alt="image" src="https://github.com/user-attachments/assets/12cf0767-91e9-4d60-bb33-084855a7f1d1" />

OBSERVATIONS 
•	When Vin = Vdd (High) ---> NMOS will turn on as |Vgs| > |Vt| satisfied for NMOS but not for PMOS – PMOS will turn off
•	When Vin = Vss (Low) ---> PMOS will turn on as |Vgs| > |Vt| satisfied for PMOS but not for NMOS – NMOS will turn off

FOR THE NMOS 
VGSn = VIN
VDSn = Vout
FOR THE PMOS 
VGSp = VIN - VDD 
VDSP = VOUT - VDD 

FOR THE RELTIONSHIP BETWEEN CURRENT 
IDSP = - IDSN

<img width="611" height="474" alt="image" src="https://github.com/user-attachments/assets/c93f1022-596a-4f3a-9a90-430b9a3fd6ce" />

<img width="633" height="342" alt="image" src="https://github.com/user-attachments/assets/bc3dc765-c800-43aa-8d54-a2744e131dd2" />


<img width="940" height="300" alt="image" src="https://github.com/user-attachments/assets/8e0a8fe1-5f2e-4d53-b74b-08e0d8da7315" />

 Vout = 2V, output capacitor is fully charges there is no charging current flowing to output capacitor, there is 0 current here, the load curve is in form of Vin Vout and IdsN for PMOS

<img width="708" height="301" alt="image" src="https://github.com/user-attachments/assets/3b01d1e5-efb3-462f-9668-ab1a969807c2" />

WE HAVE TO MERGE BOTH THE GRAPH AND SELECT THE INTERSECTION POINT FOR VIN 

<img width="629" height="392" alt="image" src="https://github.com/user-attachments/assets/e42efa2a-a9ea-44ae-aa9a-e6407d855148" />

TO PLOT VTC WE NEED NMOS AND PMOS TO SELECT THE PRTUCUALR REGION OF OPERATION 

So the range of Vin and Vout is 0V-2V.

When Vin = 0V, Vout = 2V; NMOS is Cut Off and PMOS is in Linear region
When Vin = 0.5V, 1.5V<Vout<2V; NMOS is in Saturation region and PMOS is in Linear region.
When Vin = 1V, 0.5V<Vout<1.5V; NMOS and PMOS are in Saturation region.
When Vin = 1.5V, 0<Vout<0.5V; NMOS is Linear region and PMOS is in Saturation region.
When Vin = 2V, Vout = 0V; NMOS is in linear region and PMOS is Cut Off

<img width="940" height="581" alt="image" src="https://github.com/user-attachments/assets/d8def3d6-4449-4410-a299-7fa975afc5cd" />


DAY 3 /README.md


CMOS SWITCHING VTH AND DYNAMIC SIMULATIONS 

L1 SPICE deck creation for CMOS inverter

We will now simulate the VTC. For that we need to create the SPICE deck. It is a connectivity information (Netlist). As there is information about substrate, the circuit is as shown below.Here M1 is PMOS and M2 is NMOS

<img width="546" height="501" alt="image" src="https://github.com/user-attachments/assets/72678b8a-d8c0-4f95-9a8e-01aac7041637" />

KEEPING W/L FOR BOTH NMOS AND PMOS 

<img width="686" height="538" alt="image" src="https://github.com/user-attachments/assets/151fc1fe-d21e-40b3-897e-a064a49776e0" />

VIN AND VOUT IS THE NEXT STEP 

<img width="683" height="548" alt="image" src="https://github.com/user-attachments/assets/b66ba3c8-b440-45b1-bee5-52ad031e4778" />

NODE IDENTIFICATION  , IT THE POINT WHERE 2 COMPONENT MEET 

<img width="700" height="476" alt="image" src="https://github.com/user-attachments/assets/7b72c076-09b6-427c-85a6-958324f0e937" />

PMOS AND CMOS IS THERE , pmos connected to the vdd , the point of pmos and nmos there is a capacitor connected , there is one single input vin , the input , nmos , capacitor and vdd conndcted to ground 

vin = 2.5 v , vdd = 2.5 v
w/l for pmos = 0.375/0.25u for M1
w/l for nmos = 0.375/0.25u for M2 
c = 10f F
vout = v at capacitor 
 
DGSS 
used in cmos for gate to source leakge current (igss) or gate to source breakdown voltage (vgs rating) , standard term IGSS , it is the current that flows from gate to source whenn a voltage is applied between gate and source 
IGss = IG when VDs = 0 

lecture 2 spice simulation 

<img width="687" height="328" alt="image" src="https://github.com/user-attachments/assets/7ffd993f-b265-4c27-881e-c609fa7c088f" />


<img width="702" height="323" alt="image" src="https://github.com/user-attachments/assets/d8f1d50f-1b2b-47c9-ada0-fff4049804e5" />


<img width="690" height="317" alt="image" src="https://github.com/user-attachments/assets/9b539da1-e58e-42d2-8e59-d3d1369623ad" />

Next comes the Simulation Commands
Here we will be sweeping the gate input voltage from 0 to 2.5V with steps of 0.05. We need to find the VTC, for this only we will be sweeping the input voltage and measuring the output voltage.
Final step is to describe the Model files, all the information about the technological parameteres is given inside the model files.

<img width="677" height="326" alt="image" src="https://github.com/user-attachments/assets/1fdfdc88-de49-4d1c-8c16-68fcdb11d136" />

Now we will do the SPICE simulation for Wn=Wp=0.375u, Ln=Lp=0.25u, Wn/ln=Wp/Lp=1.5. Below is the VTC we get for the above netlist.

<img width="705" height="517" alt="image" src="https://github.com/user-attachments/assets/a9b9d164-cce6-45e1-8134-fa8ed7a86281" />

get the VTC for Wn= 0.375u, Wp= 0.9375u, Ln,p=0.25u; Wn/Ln=1.5, Wp/Lp=2.5 (PMOS width is 2.5 times more than NMOS)

<img width="698" height="532" alt="image" src="https://github.com/user-attachments/assets/e2fad427-2ed3-41f7-a63e-f625f6d9f283" />

shift in graph left side shift , because nmos is more stronger than pmos.

LECTURE 3 
SIMULATION 
FOR VTC OF CMOS 

*Model Description
.param temp=27

*Including sky130 library files
.lib "sky130_fd_pr/models/sky130.lib.spice" tt

*Netlist Description

XM1 out in vdd vdd sky130_fd_pr__pfet_01v8 w=0.84 l=0.15
XM2 out in 0 0 sky130_fd_pr__nfet_01v8 w=0.36 l=0.15

Cload out 0 50fF

Vdd vdd 0 1.8V
Vin in 0 1.8V

*simulation commands

.op

.dc Vin 0 1.8 0.01

.control
run
setplot dc1
display
.endc

.end

<img width="692" height="380" alt="image" src="https://github.com/user-attachments/assets/7ca5a8b5-c879-441d-b222-2d8f9499c42f" />

<img width="1920" height="1031" alt="image" src="https://github.com/user-attachments/assets/f98cc3b1-088c-4cda-b5cf-744031966e8e" /> 

<img width="1918" height="1076" alt="image" src="https://github.com/user-attachments/assets/24bcc7db-d01c-4c9c-8d20-69d2fde0bb3b" />

So switching threshold for W/L=2.3 is around 0.876V
<img width="280" height="30" alt="image" src="https://github.com/user-attachments/assets/361f7fe8-9f34-47a0-9836-2f9b1bf2c662" />

To find the switching threshold voltage (Vm), it is known that Vout = Vin so zoom in on the plot where roughly Vout = Vin by selecting the area of the plot by right clicking on the screen and dragging it to select the area.
Zoom twice or thrice until the point where Vm lies becomes almost certain.
Left click roughly on the point on the curve where Vm should approximately lie.
Values of x0 and y0 will now appear on the terminal window.
Since we are finding Vm, therefore x0 ~ y0 and hence x0=y0=Vm.

FOR TRANSIENT ANALYSIS 

*Model Description
.param temp=27

*Including sky130 library files
.lib "sky130_fd_pr/models/sky130.lib.spice" tt

*Netlist Description

XM1 out in vdd vdd sky130_fd_pr__pfet_01v8 w=0.84 l=0.15
XM2 out in 0 0 sky130_fd_pr__nfet_01v8 w=0.36 l=0.15

Cload out 0 50fF

Vdd vdd 0 1.8V
Vin in 0 PULSE(0V 1.8V 0 0.1ns 0.1ns 2ns 4ns)

*simulation commands

.tran 1n 10n

.control
run
.endc

.end


<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/4e191603-927c-4c85-a067-97835b8e498e" />


<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/1f8a2313-818e-4c61-9022-94f424bf2ce5" /> 

<img width="305" height="67" alt="image" src="https://github.com/user-attachments/assets/1c25b61b-6df2-4520-9056-f3400829b9de" />


Zoom on the part of the curve having fall of the input pulse and rise of the output pulse around voltage of (Vdd/2) by right clicking on the screen and dragging it to select the area.
Now, left click on the rising edge of the output curve at (Vdd/2) to get a point x0,y0 on the terminal.
Similarly, get the point at (Vdd/2) for falling edge of the input curve.
The difference between the x-coordinate of the rising edge of the output curve and the falling edge of the input curve is the rise delay.
To calculate the falling delay:
Zoom on the part of the curve having rise of the input pulse and fall of the output pulse around voltage of (Vdd/2) by right clicking on the screen and dragging it to select the area.
Now, left click on the falling edge of the output curve at (Vdd/2) to get a point x0,y0 on the terminal.
Similarly, get the point at (Vdd/2) for rising edge of the input curve.
The difference between the x-coordinate of the falling edge of the output curve and the rising edge of the input curve is the fall delay.

PART 2 
STATIC BEHAVIOUR EVALUTION CMOS INVERTER , SWITCHING THRESHOLD 

Static Behavior Evaluation: CMOS Inverter Robustness

Switching Threshold
Noise Margin
Power Supply Variation
Device Variation

Switching Threshold (Vm)

It is the point where Vin = Vout

Graphical method to find Vm is to draw a line across the graph of output voltage to input voltage of a CMOS inverter starting at the origin and ending at the opposite diagonal of the plot (basically a line with a 45 degree inclination with the x-axis)the x-coordinate of the point of intersection of this line and the curve is the switching threshold.

Vm when (Wp/Lp) is 1.5 is approximately equal to 0.98V and when (Wp/Lp) is 3.75 it is approximately equal to 1.2V

Wp and Lp in the above section are Width of PMOS channel and Length of PMOS channel

both PMOS and NMOS are turned 'ON' because Vgs almost crossed the threshold region for both of them.

 Vgs = Vds
IdsP = - IdsN which means that IdsP + IdsN = 0

<img width="394" height="133" alt="image" src="https://github.com/user-attachments/assets/37f843b5-44b3-4fe0-8da3-bd754effc5a5" />

IGNORE 1+LAMDA VDS , THE TERM IS VERY SMALL AND CALCULATION WIIL BE HARD.

IdsP + IdsN = 0
<img width="632" height="67" alt="image" src="https://github.com/user-attachments/assets/0031a3f8-2527-4862-baec-8859cc26f67a" />

<img width="342" height="147" alt="image" src="https://github.com/user-attachments/assets/c4bf24e1-4da0-44e6-be94-970691d0f8c2" />

RATIO OF PMOS VS NMOS TX 
IdsN = -IdsP 

<img width="627" height="405" alt="image" src="https://github.com/user-attachments/assets/e95affa9-d40e-4681-ba6e-5a99d0bd4e28" />

Wp is the width of the channel in PMOS
Lp is the length of the channel in PMOS
Wn is the width of the channel in NMOS
Ln is the length of the channel in NMOS
kn' is the process transconductance of the NMOS
kp' is the process transconductance of the PMOS
Vdsatn is the Vdsat of the NMOS
Vdsatp is the Vdsat of the PMOS
Vm is the switching threshold voltage
Vt is the threshold voltage
Vdd is the supply voltage


(Wp/Lp)	 x.(Wn/Ln)	Rise Delay	Fall Delay	Vm
(Wp/Lp)	 1.(Wn/Ln)	 148pS	     71pS	    0.99V
(Wp/Lp)	 2.(Wn/Ln)	 80pS	    76pS	     1.2V
(Wp/Lp)	 3.(Wn/Ln)	 57pS	    80pS	     1.25V
(Wp/Lp)	 4.(Wn/Ln)	 45pS	    84pS	     1.35V
(Wp/Lp)	 5.(Wn/Ln)	 37pS	    88pS	     1.4V

When (Wp/Lp) = 2.(Wn/Ln), there is an approximately equal rise-fall delay
Due to the equal rise-fall delay, (Wp/Lp) = 2.(Wn/Ln) create typical characteristics for a clock inverter/buffer
The conditions other than (Wp/Lp) = 2.(Wn/Ln) can still be used as regular inverters/buffers and these can be preferred for data path
Switching Threshold for (Wp/Lp) = 2.(Wn/Ln) and (Wp/Lp) = 3.(Wn/Ln) is very small. Similarly, switching threshold for (Wp/Lp) = 4.(Wn/Ln) and (Wp/Lp) = 5.(Wn/Ln) is also very small
When Wp/Lp is increased, the rise delay is isgnificantly reduced because time required for the output capacitor to charge decreases significantly and the reason is the availability of a bigger area to charge the capacitor.

Ron(PMOS) = 2.5*Ron(NMOS)


DAY 4 /README.md


CMOS NOSISE MARGIN 

<img width="719" height="1600" alt="image" src="https://github.com/user-attachments/assets/67baca87-ae1e-4b40-b001-e33c689ec967" />
going towards positive vdd the output goes to 0.

<img width="719" height="1600" alt="image" src="https://github.com/user-attachments/assets/12553b99-0d22-455e-8783-ae9fabf8a9da" />

there is sudden shift at vdd/2 , this is infinite slope. 
slope of area = vout change / vin change 
but at vdd/2 there is no change there is sudden drop , 0 change 
idelly infinite 

<img width="719" height="1600" alt="image" src="https://github.com/user-attachments/assets/6c57d7cd-67cc-4b84-97c4-bba0a56714fa" />

<img width="719" height="1600" alt="image" src="https://github.com/user-attachments/assets/e219ab94-0431-4570-8530-49f0f4ce4a45" />

the resistance and capacitance stops the sudden change , it takes time to shift , so there is a slope that defines delay.
this graph is also not correct 

<img width="719" height="1600" alt="image" src="https://github.com/user-attachments/assets/fd7cbbc9-e92f-4288-aa4c-209d12cbd14c" />

<img width="719" height="1600" alt="image" src="https://github.com/user-attachments/assets/7ef9bddb-119b-455b-954c-fc24d8f8ad09" />

<img width="719" height="1600" alt="image" src="https://github.com/user-attachments/assets/beaa9fdf-5608-4c9c-b46e-55d25cc45f6c" />

in these image all parameters are defined that are necessary.

<img width="719" height="1600" alt="image" src="https://github.com/user-attachments/assets/b937ad13-acac-4664-bb8e-496850220432" />

<img width="719" height="1600" alt="image" src="https://github.com/user-attachments/assets/33c16e89-59d6-4d37-be7a-7d4e4e0a367f" />

<img width="719" height="1600" alt="image" src="https://github.com/user-attachments/assets/79ce07a3-2100-4b89-9cc6-2cada1c16c35" />

in these 3 images we have gone through more practical way of analysing of the graph. 

<img width="719" height="1600" alt="image" src="https://github.com/user-attachments/assets/38cc2ffe-a5e7-4c27-88c7-e4be7dee18d2" />

<img width="719" height="1600" alt="image" src="https://github.com/user-attachments/assets/ebe11dbd-429b-44e9-9134-5ff422dcf7ac" />

<img width="719" height="1600" alt="image" src="https://github.com/user-attachments/assets/4cba86d9-44af-454b-b836-b42cda43e4c4" />

<img width="719" height="1600" alt="image" src="https://github.com/user-attachments/assets/c31fe84f-e04d-4322-9e34-a9bfe6ca99fc" />

For any signal to be considered as logic '0' and logic '1', it should be in the NMl and NMh ranges, respectively. - If the height of the bump lies in between Vol and Vil then it's not hazardous because it still lies in the range of logic '0'. Any glitch that occurs in this region is a safe glitch because it will still be considered as logic '0'. - If the height of the bump lies in the "undefined region" then it is potentially hazardous because it can acquire logic '1' which can be fatal. Any glitch in this region is unsafe because it is unclear if it will go to logic '1' or fall to logic '0'. - If the height of the bump lies in between Vih and Voh then it will definitely be considered as logic '1'. These kinds of glitches are the glitches that need to be fixed. 


(Wp/Lp)	  x.(Wn/Ln)	 high rail     low rail	       Vm
(Wp/Lp)	  1.(Wn/Ln)	    0.3	       0.3	        0.99V
(Wp/Lp)	  2.(Wn/Ln)	   0.35	       0.3	        1.2V
(Wp/Lp)	  3.(Wn/Ln)	    0.4	       0.3	        1.25V
(Wp/Lp)   4.(Wn/Ln)	   0.42	       0.27	        1.35V
(Wp/Lp)	  5.(Wn/Ln)	   0.42	       0.27	        1.4V

this is out put swing not noise margin , as the formula for noise margin is different that is stated in above lecture , this is output swing that the input of our mosfet is like that out put does not chip. 

<img width="615" height="457" alt="image" src="https://github.com/user-attachments/assets/4f5b8b0e-34e8-4b9d-b41e-cdada4e8a79d" />

this is for digital design 

LAB DAY 4 
*Model Description
.param temp=27

*Including sky130 library files
.lib "sky130_fd_pr/models/sky130.lib.spice" tt

*Netlist Description

XM1 out in vdd vdd sky130_fd_pr__pfet_01v8 w=1 l=0.15
XM2 out in 0 0 sky130_fd_pr__nfet_01v8 w=0.36 l=0.15

Cload out 0 50fF

Vdd vdd 0 1.8V
Vin in 0 1.8V

*simulation commands

.op

.dc Vin 0 1.8 0.01

.control
run
setplot dc1
display
.endc

.end

<img width="1920" height="1030" alt="image" src="https://github.com/user-attachments/assets/a668db78-2821-46fa-9d33-6e402304893c" />

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/480a7484-c42c-4baf-8bdd-ad8c816c76cb" />

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/3b409a79-a3c4-4b85-ab96-de847e2c6804" />

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/1635e405-dd25-4f18-b83c-36ad3552d514" />

 x0 = 0.766667, y0 = 1.71351
Now, left click on the point towards the bottom of the graph where the curvature seems to be '-1'
In this case it was x0 = 0.977333, y0 = 0.110811. Let's consider these points as x1 and y1 thus making the coordinates x1 = 0.977333, y1 = 0.110811
For noise margin high we need Voh-Vih and in this case Voh=y0 and Vih=x1
For noise margin low we need Vil-Vol and in this case Vil=x0 and Vol=y1
NMh = 0.736177 and NMl = 0.655856


Day 5/README.md

: CMOS Power supply and
Static behaviour evaluation-CMOS inverter robustness-Power supply variation

LAB 
FOR POWER SUPPLY 

*Model Description
.param temp=27

*Including sky130 library files
.lib "sky130_fd_pr/models/sky130.lib.spice" tt

*Netlist Description

XM1 out in vdd vdd sky130_fd_pr__pfet_01v8 w=1 l=0.15
XM2 out in 0 0 sky130_fd_pr__nfet_01v8 w=0.36 l=0.15

Cload out 0 50fF

Vdd vdd 0 1.8V
Vin in 0 1.8V

.control

let powersupply = 1.8
alter Vdd = powersupply
        let voltagesupplyvariation = 0
        dowhile voltagesupplyvariation < 6
        dc Vin 0 1.8 0.01
        let powersupply = powersupply - 0.2
        alter Vdd = powersupply
        let voltagesupplyvariation = voltagesupplyvariation + 1
      end

plot dc1.out vs in dc2.out vs in dc3.out vs in dc4.out vs in dc5.out vs in dc6.out vs in xlabel "input voltage(V)" ylabel "output voltage(V)" title "Inveter dc characteristics as a function of supply voltage"

.endc

.end

<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/53906cab-71f5-418a-b75a-754274b05630" />

<img width="1600" height="831" alt="image" src="https://github.com/user-attachments/assets/733573da-0bd7-404d-9d26-daa4db37a07e" />

 x0 = 0.766667, y0 = 1.71351
The poiNT x0 = 0.982667, y0 = 0.1
coordinates of the point to be x1, y1
 the point becomes x1 = 0.982667, y1 = 0.1
Subtract y1 from y0. So, y0 - y1 = 1.61351
Subtract x1 from x0. So, x0 - x1 = -0.216
Now, gain = (y0-y1)/(x0-x1)
Gain(g) = |(1.61351)/(-0.216)| = |-7.46995| = 7.46995

PART 2 STATIC BEHAVIOUR 

Etching Process Variation:

The etching process will define the structures in the layout of the CMOS inverter.
Etching is a very important fabrication step
It is the process that defines the structure (width and the height)
Based on the structures that get defined by the process, it directly impacts the delay
In layout of the CMOS inverter we have:

P-diffusion region which is indicated by green color.
Poly-silicon area which is indicated by red color.
Metal layer which is indicated by blue color.
N-diffusion region indicated by yellow color.
Contacts between two layers indicated by black crosses.
Thickness of poly-silicon layer is the gate length annd it defiens at which node we are (20nm, 30nm, 45nm, etc.).

Thickness of the P-diffusion layer is the width of the gate of the PMOS and the thickness of the N-diffusion layer is the width of the gate of the NMOS.

Width identifies overlap area between the diffusion layer and the poly-silicon layer.

Fabrication is basically a lab where we have a lot of things like chemicals, water, gases, etc. running and due to these the ideal structure is distorted.

<img width="680" height="312" alt="image" src="https://github.com/user-attachments/assets/9a2364de-cfc1-441a-8037-b36c4a6b7a0a" />

<img width="687" height="705" alt="image" src="https://github.com/user-attachments/assets/7c165087-c22d-40d8-8cce-3a13c2858f64" />

<img width="640" height="370" alt="image" src="https://github.com/user-attachments/assets/b725519f-cab3-4506-8a08-b4a3441a96a0" />

THIS IS HOW THE CURRENT CAN CHANGE 

OXIDE 
Oxide Thickness:

In an ideal oxidation process, the gate oxide thickness will be constant throughout the process.
In real oxidation process, the gate oxide thickness will not be constant along the gate length.
In an inverter chain, the gate oxide thickness can vary for each transistor.
Oxide thickness directly affects the Id equation because Cox is dependant on it.
Strong PMOS:

PMOS with less resistance (possibly least resistance if the size chosen is the greatest size possible)
PMOS is wider in size (possibly widest PMOS available)
Weak NMOS:

NMOS with high resistance (possibly highest resistance if the size chosen is the least size possible)
NMOS is small in size (possibly smallest NMOS available)
Strong NMOS:

NMOS with less resistance (possibly least resistance if the size chosen is the greatest size possible)
NMOS is wider in size (possibly widest NMOS available)
Weak PMOS:

PMOS with high resistance (possibly highest resistance if the size chosen is the least size possible)
PMOS is small in size (possibly smallest PMOS available)
With the variation from Weak PMOS - Strong NMOS to Strong PMOS - Weak NMOS, the switching threshold varies from roughly 0.7V to 1.4V which is fairly acceptable because behavior of the inverter is intact

LAB 

*Model Description
.param temp=27

*Including sky130 library files
.lib "sky130_fd_pr/models/sky130.lib.spice" tt

*Netlist Description

XM1 out in vdd vdd sky130_fd_pr__pfet_01v8 w=7 l=0.15
XM2 out in 0 0 sky130_fd_pr__nfet_01v8 w=0.42 l=0.15

Cload out 0 50fF

Vdd vdd 0 1.8V
Vin in 0 1.8V

*simulation commands

.op

.dc Vin 0 1.8 0.01

.control
run
setplot dc1
display
.endc

.end

<img width="1920" height="1031" alt="image" src="https://github.com/user-attachments/assets/64b3bb75-c62d-4f35-ab22-bc23d3311a8e" />

<img width="1920" height="1029" alt="image" src="https://github.com/user-attachments/assets/57867d47-93bd-44e1-a409-254868a4851f" />

 x0 = 0.988209, y0 = 0.988191 is obtained
x0 ~ y0.
Switching Threshold Voltage = Vm = x0 = y0 = 0.988V











