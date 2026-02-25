# CMOS-DESIGN-
Day 1
 NMOS Id vs Vds

CIRCUIT DESIGN AND SIMULATION      
CIRCUIT DESIGN 

Logic Gates, Inverters, Buffers ARE MADE FROM PMOS/NMOS AND Connected TO perform functions 

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

 Seems like – Id constant current – all parameters are constant - Not true – but has dependency on L and L has dependency VDS – Accurate equation requires to incorporate the effect of VDS 
 
