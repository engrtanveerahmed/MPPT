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

##Higher level Diagram

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

![]()

##### INA213 (Current sense amplifier):
The INA21x are voltage-output, current-shunt monitors (also called current-sense amplifiers) that are commonly used for overcurrent protection, precision-current measurement for system optimization, or in closed-loop feedback circuits. This series of devices can sense drops across shunts at common-mode voltages from 0.3 V to 26 V, independent of the supply voltage. Six fixed gains are available: 50 V/V, 75 V/V, 100 V/V, 200 V/V, 500 V/V, or 1000 V/V. The low offset of the zero-drift architecture enables current sensing with maximum drops across the shunt as low as 10-mV full-scale. These devices operate from a single 2.7-V to 26-V power supply, drawing a maximum of 100 uA of supply current. All versions are specified over the extended operating temperature range (40°C to +125°C), and offered in SC70 and UQFN packages. We have used this componant as to sense the input and output voltage/current to track the working of the MPPT.

![]()

##### IR2104 (Half-bridge):
The discrete Half-bridge driver based on IR2104 gate driver IC and low impedance high current N channel IRFP4368 MOSFETS , The IR2104 is a high voltage, high speed power MOSFET driver with independent high and low side referenced output channels. We have used this componant to derive the mosfets.

![]()

##### Schottky Diode :
The Schottky Diode is a type of semiconductor diode which have the advantage that their forward voltage drop is substantially less than that of the conventional silicon pn-junction diode. Schottky diodes have many useful applications from rectification, signal conditioning and switching, through to TTL and CMOS logic gates due mainly to their low power and fast switching speeds.

##### IPB136n08n3 (PWR-MOSFET):
These are ideal for high frequency switching. Optimized technology for DC/DC converters. Excellent gate charge x R product N-channel, normal level. 100% avalanche tested. Pb-free plating; RoHs compliant.


Shunt Resistors:
Shunt resistors are used with current sense amplifier to sense the current.

##### Voltage Regulator LM7805:
We are using this voltage regulator because the input voltage is 12 voltages and our microcintroller and some other componants run on 5V so its is regulating the voltages. It is easily available for use.



##### Zener Diode::
We are using zener diode if our input voltage increases from the circuit limitations, it will directly ground the voltages.

###### Connectivity to components (Protocol)
As we have used Atmega32U4 microcontroller, which has the support to connect a USB, so we are using Universal serial bus for the connectivity of our board with PC to burn the code into it.
## Electrical Schematic
The schematic diagram is taken from the Eagle file we have developed for our final PCB:
