# Maximum Power Point Tracking (MPPT)

## Introduction
We know that sun light is varriable during day some time is low some time it's intensity is high specially at mid of day its intensity is high due to this our solar pannel gives varriable voltages we intensity is high our normal solar pannel 12 voltes rated  gives 14or 15 voltages and if it is connected to 12v rated bettery this extra voltages is really hazerd for our bettry in ordr to remove this hazerd we design Maximun power point trackin solar charge controller (MPPT).

## Design requirements
In todays world design in project play inportant it requires to main key parameters one is we can carry it any where easily number two it is eye catching, in order to do we made design on autocade and also we are blessed with fablab that contain 3D printer with help of that we made our 3D design

![This is an image](https://github.com/engrtanveerahmed/MPPT/blob/main/auto%20cade%20design%20pics/req.jpeg?raw=true)

## Project excuting plan
We have distribute our task in to two member so that beacause in short time we have alot of work to do bellow chart contain our flow of doing work. 

![This is an image](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/excutint%20plan.PNG?raw=true)

## Destributinsion of tasks

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/task%20distributins.PNG?raw=true)

## Higher level Diagram

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/BD.png?raw=true)

## Description of Principle of Operations
MPPT Min work is to gives stable (12)voltageg at out put this work (step down) is done by the buck converter, at in put and out we used voltage and current sensior; voltages divder circuit at input and output Which sensed voltages developed on the input and gives it to an analogue pin of microcontroller. also a current sense amplifier is attached using a shunt resistor on the main input section. There is also a voltage divider circuit on the output section where the battery is connected. A current sense amplifier is used on the output section as well. These all values are fed to the microcontroller. Depending upon these values, microcontroller decides about the PWM signal fed to the Half-Bridge Mosfet Driver IC. this IC takes input as a PWM signal and switches the MOSFETs with a very high speed. The Buck converter acts according to the decission made by microcontroller depending upon the input and output currents and voltages.

## Bill of material
![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/bill%20of%20material.PNG?raw=true)

## Desciption of Major Components of project
##### Microcontroller:

The low-power Microchip 8-bit AVR RISC-based microcontroller featuring 32KB self-programming flash program memory, 2.5KB SRAM, 1KB EEPROM, USB 2.0 full-speed/low speed device, 12-channel 10-bit A/D-converter, and JTAG interface for on-chip-debug. The device achieves up to 16 MIPS throughput at 16 MHz. 2.7 - 5.5 Volt operation. We have used this microcontroller because of its lower consemption and usb support. its features helped us to replace arduino with this microcintroller in project.
![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/micro%20controller.PNG?raw=true)

###### USB mini:
The small USB is used in digitil devices like digital cameras, external hard drives, USB hubs and other equipment. Mini USB is much smaller than USB Type A and B but twice as thick as Micro USB. We have used this componant as we could burn our code easily on the microcontroller.

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/usb%20min.PNG?raw=true)

##### INA213 (Current sense amplifier):
The INA21x are voltage-output, current-shunt monitors (also called current-sense amplifiers) that are commonly used for overcurrent protection, precision-current measurement for system optimization, or in closed-loop feedback circuits. This series of devices can sense drops across shunts at common-mode voltages from 0.3 V to 26 V, independent of the supply voltage. Six fixed gains are available: 50 V/V, 75 V/V, 100 V/V, 200 V/V, 500 V/V, or 1000 V/V. The low offset of the zero-drift architecture enables current sensing with maximum drops across the shunt as low as 10-mV full-scale. These devices operate from a single 2.7-V to 26-V power supply, drawing a maximum of 100 uA of supply current. All versions are specified over the extended operating temperature range (40°C to +125°C), and offered in SC70 and UQFN packages. We have used this componant as to sense the input and output voltage/current to track the working of the MPPT.

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/ir2104.png?raw=true)

##### IR2104 (Half-bridge):
The discrete Half-bridge driver based on IR2104 gate driver IC and low impedance high current N channel IRFP4368 MOSFETS , The IR2104 is a high voltage, high speed power MOSFET driver with independent high and low side referenced output channels. We have used this componant to derive the mosfets.

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/ir2104.png?raw=true)

##### Schottky Diode :
The Schottky Diode is a type of semiconductor diode which have the advantage that their forward voltage drop is substantially less than that of the conventional silicon pn-junction diode. Schottky diodes have many useful applications from rectification, signal conditioning and switching, through to TTL and CMOS logic gates due mainly to their low power and fast switching speeds.

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/shottky.jpg?raw=true))


##### IPB136n08n3 (PWR-MOSFET):
These are ideal for high frequency switching. Optimized technology for DC/DC converters. Excellent gate charge x R product N-channel, normal level. 100% avalanche tested. Pb-free plating; RoHs compliant.

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/PowerMosfet.jpg?raw=true))

Shunt Resistors:
Shunt resistors are used with current sense amplifier to sense the current.

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/ShuntResistor.jpg?raw=true)

##### Voltage Regulator LM7805:
We are using this voltage regulator because the input voltage is 12 voltages and our microcintroller and some other componants run on 5V so its is regulating the voltages. It is easily available for use.

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/VR_LM7805.jpg?raw=true)

##### Zener Diode::
We are using zener diode if our input voltage increases from the circuit limitations, it will directly ground the voltages.

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/Zener.jpg?raw=true)

###### Connectivity to components (Protocol)
As we have used Atmega32U4 microcontroller, which has the support to connect a USB, so we are using Universal serial bus for the connectivity of our board with PC to burn the code into it.
## Electrical Schematic
The schematic diagram is taken from the Eagle file we have developed for our final PCB:

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/ss%20schematic.PNG?raw=true)


## Brief Description of Schematic
Here we define our project more clearily.

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/ss%20of%20schematic%20design%20eagle.PNG?raw=true)

##### Microcontroller and its required components:
The microcontroller is the key component of this whole circuit as it is making decissions on the basis of values it is receiving. the components attached with microcontroller in "1" are chosen according to the Arduino Leonardo which uses the same Microcontroller. An ICSP header is also connected to burn the boadloader on to the microcontroller. The connection of a USB MINI are also made with the microcontroller.

##### Input Voltage Divider Circuit:
This circuit divides the input voltage to such a level in which microcontroller can sense it because if we attach the microcontroller directly, it cannot bear the voltage and will burnout intantly. So we have to reduce the voltage to such a level which can be given to microcontroller. We used a 39kiloohm resistor and a 10 kilo ohm resistor to make the ratio appropriate. Also two zener voltages are connected in parallel for we want input voltage not more than a certain value.
##### Input Current Sense Amplifier:
INA213, a current sense amplifier is connected here to sense the input current. The shunt resistor helps this IC to sense the current and then this IC gives output to the Microcontroller which then displays it on the LCD.

##### Half Bridge Driver IC and Buck Converter:
The IR2104, a half bridge MOSFET driver takes input of PWM signal from the microcontroller and then performs the switching of the MOSFETs. Hence controlling the output current and voltage.

##### Output Current Sense Amplifier:
It works on the same principle as the input current sense amplifier.

##### Output Voltage Regulator:
Volatge regulator is developed here for the same reason, the only difference is the voltage for division. Here the voltage is 12V. So, we connected a 22 kilo-ohm resistor in series with a 10 kilo-ohm resistor.

##### LCD connectors:
these connectors are attached for the display which will be mounted on the casing.

##### Power Headers and Voltage Regulator:
The three headers for 12 volts Supply(on which the board will operate), Panel(to take input from solar panel) and Output(for the output voltage taken from the circuitry ). The voltage regulator is connected because we are using 12V supply on which the IC IR2104 operates but all other ICs need 5V to operate so we are using this LM7805 for this purpose.


## PCB Layout

![](https://github.com/engrtanveerahmed/MPPT/blob/main/autocad%20schematic.PNG?raw=true)

We used Eagle software to develop the PCB for our project and we created the layouts in .PNG formats as the Milling Machine available in Fablab needs picture format for its processing. Following is the final PCB layout:

## Challenges While Routing
Whille routing the PCB it consumed a lot of out time because the circuit we were following used a separate board for microcontroller but our aim was to embed both the circuit on a single layer, making it more compact. This came with lots of hurdles while routing, we used few zero ohm resitor to overcome routing issues and at the end developed a lot more compact circuit after tens of attempts.


## Bill of Material on taped on a Paper
Following is the Picture of the components taken from the FabLab

![](https://github.com/engrtanveerahmed/MPPT/blob/main/autocad%20schematic.PNG?raw=true)

## Picture of Clean Printed Circuit Board
For fabrication of our PCB, we used SRM-20(Rolland's mills) machine. It needs a monochrome picture for its processing. the monochrome picture we took from Eagle software were then uploaded to the "Fab-Modules.org" and then we generated the ".rml" files needed for SRM-20 to process the milling.

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/full%20cirsuit%20(3).jpeg?raw=true)

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/circut%20board1.jpeg?raw=true)


## Picture of Populated Circuited Board
After fully soldering teh components, our board looked like this:

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/full%20cirsuit%20(1).jpeg?raw=true)


## Procedure adopted to burn Bootloader
To burn the boot loader on to the microcontroller, we used ICSP header and arduino IDE. we burnt the bootloader of Arduino leonardo onto the ATmega32U4. For this we followed the following steps:
1. connetcing th board with PC through ICSP header and a USB mini cable for further burning the test code.
2. selecting the board through "Tools" menu.
3. in tools, further going to submenu "Select Board".
4. selecting "Arduino Leonardo".
5. again going to "tools" menu and then selecting the submenu "Port" and then select the port on which ICSP is connected.
6. again going to another submenu "Programmer" and selecting "AVRISP mkll" .
7. last step is to select the last most option of "burn the bootloader".
8. wait for few minutes till it shows the message on status bar as "Done burning Bootloader.".

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/b.jpeg)


## Picture of successfully operating circuit

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/R1.PNG)


## Picture of fully assembled System

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/full%20cirsuit%20(7).jpeg)


## The FlowChart of our software design

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/Software_flowchart.png)


## Main Functions of the code
##### buck_setup() Function::
This function is designed to set up the timer to generate PWM signal. It initializes the timer with the desired duty cycle to set the circuit up.
##### buck_enable() Function:
This method is written so to enable the clock source and then turns on the Half bridge driver through PWM signal.
##### buck_disable() Function:
TThis functtion turns off the clock source and sets the duty cycle of PWM signal to zero.
##### buck_duty(unit8_t duty) Function:
This function checks the duty cycle of the and stes it to the appropriate value for the operation of the Buck converter. it Arranges the duty cycle to an optimum level.
##### write_display() Function:
This function is utlized to write on the LCD. it tfakes values from several values and displays them along with some text on the LCD.
##### read_values() Function:
This function takes the values from the volatge divider circuits and current sense amplifiers and sets them correctly after callibration.
##### buck_update() Function:
This method is the key function in the code which calls some of the above functions and updates the duty cucle accordingly.


## Challenges faced while coding
The major problem we faced during the coding for this project was configuring the timer for generatng PWM signal. We tried to configure different available timers using different PWM pins on the board. First we configured timer1 using PWM pin 9, but this timer was a 16 bit timer which brought a lot of problems because our major calculations were based on the 8 bit timer. so after struggling a lot we obtained a maximum volatge of 7.44V at the output. Furthermore we connected our Half bridge driver with PWM pin 11 and using timer0 we obtained the exact output.


## CAD Design of Enclosure
For Casing of our prodcut, we used both laser Cut and 3D-printing. We wanted to consume lesser filament for 3D-printing thats why we thought of making the top of the casing clear to make it a bit unique. So, we made the top using laser cut. We designed a locking mechanism of Slide and press. We slide one side of the top and press the other towards the bottom.


## CAD Design with Dimensions
Followings are the CAD design pictures with dimensions:

![](https://github.com/engrtanveerahmed/MPPT/blob/main/auto%20cade%20design%20pics/mm1.PNG)

![](https://github.com/engrtanveerahmed/MPPT/blob/main/auto%20cade%20design%20pics/mmb.PNG)

![](https://github.com/engrtanveerahmed/MPPT/blob/main/auto%20cade%20design%20pics/p2.PNG)

![](https://github.com/engrtanveerahmed/MPPT/blob/main/auto%20cade%20design%20pics/p3.PNG)


Business model

![](https://github.com/engrtanveerahmed/MPPT/blob/main/pic%20of%20major%20component/business%20model.PNG)

Every product which needs to be in the market requires a good business plan. for our product, we considered few major point regarding its cost and its users. As our project is user friendly in terms of its size, the size increases the durability. One can carry it anywhere to be used. Furthermore, solar charges(MPPT based) are very expensive products, we used such components which are commonly available and are cheap. With these two major advantages, we hope to cover a good number of users of our products when released in the market.
References
(1)soldernerd web site link review 1
https://soldernerd.com/2016/01/21/arduino-mppt-solar-charger-shield/" target

2- http://www.leonics.com/support/article2_14j/articles2_14j_en.php

3- http://ww1.microchip.com/downloads/en/DeviceDoc/Atmel-7766-8-bit-AVR-ATmega16U4-32U4_Datasheet.pdf

4. https://forum.arduino.cc/index.php?topic=125252.0

(5)Dr. Muhammad Asim Samejo (Assistant Professor at Sukkur IBA University,Pakistan)
http://www.iba-suk.edu.pk/faculty/details/INS-0011" target

(6)Engr. Aizaz Ali Larik (Lab Engineer at Sukkur IBA University,Pakistan)
http://www.iba-suk.edu.pk/faculty/details/INS-0424" target

(7)Engr. Aizaz Ali Larik (Lab Engineer at Sukkur IBA University,Pakistan)
http://www.iba-suk.edu.pk/faculty/details/INS-0424" target

(8)Nadir Ali (Fab Lab Attendant at Sukkur IBA University, Pakistan)
"nadir.ali@iba-suk.edu.pk" target

(9)Tanveer Ahmed (Stutentof Sukkur IBA University, Pakistan)
tanveerahmed.beef20@iba-suk.edu.pk" target

(10)HabibullH (Stutentof Sukkur IBA University, Pakistan)
habbibullah.beef20@iba-suk.edu.pk" target

Contact Us
Tanveer Ahmed (Undergraduate Electrical Engineering Student at Sukkur IBA University, Pakistan)

Email: tanveerahmed.beef20@iba-suk.edu.pk

Contact: +92 303 3005395 

 

Habibullah (Undergraduate Electrical Engineering Student at Sukkur IBA University, Pakistan)

Email: habibullah.beef20@iba-suk.edu.pk

Contact: +92 304 0900929 

 

Zip file containing 3D Design
Mppt Auto cade file

link contain Eagle file
Mppt Eagle file

Source Code file
Mppt Audino code

## Conclusion
This project was full of learning.We made PCB cricuit three time, the reanson in first board our USB mini port beacme short while sodering because the have small pins we learnt that do soldering carifully a single mistake can distured whole PCB, we made a seconde PCB this time we do soldering care fully but our circuit became short beacuse circuit is large so for this we check continuity test but it work was really time consuming because circuit is large finally we made last circuit it works our pervious PCB boards don not go weste we leart alot from them,but this not good practice because material goes weste we need do things carefully while making eagle file Dia of SRM matchune when it comes to microcontroller, soldering selection of component like we add big capactor which consume whole size of our PCB, We had a lot of practical interaction with our theoratical knowledge. This project proved a golden oppurtunity as we implemented most of our theoratical knowledge.Milling a PCB, designing an enclosure.etc. all of these experiences proved fruitful in increasing our skills and capabilty to do experiments and troubleshooting. In future, we have decided to continue such kind of practice for further learning and skill development.

