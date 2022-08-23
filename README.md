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
