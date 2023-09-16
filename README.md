# 10V Linear Power Supply

## Abstract

The objective of this project was to design a 10V Linear power supply with a maximum current rating of 10A. This report presents the design of a voltage regulator from scratch to drive a high-power load (100W) from a 230V input voltage.

## Introduction

Power supplies are used to drive various loads under constant voltage/current conditions. To ensure the reliable operation of a power supply several factors need to be considered including load regulation, line regulation, efficiency, protection mechanism, heat dissipation, etc.

## Design Requirements

- 10V Linear power supply with a maximum current rating of 10A
- Should include circuit protection mechanisms.
- Power supply efficiency should be considered when developing the circuit.

## Methodology

### Rectification

The first stage of the DC power supply is rectification which involves converting the input sinusoidal AC voltage to an output voltage with a single polarity. There are many different techniques for implementing the rectification stage in a circuit, however, the most used and simplest method is using a Wheatstone bridge rectifier.

### Smoothing

The second stage is smoothing which reduces the ripple voltage in the output voltage of the rectifier output.

### Regulation

#### Voltage Regulation

The voltage regulation process is a crucial aspect of a linear power supply. To achieve a constant output voltage, a virtual short circuit is utilized in this design. Virtual short circuit refers to 
configuration in a differential amplifier such as op-amp where the inverting and non-invertinginput have almost same voltage. Initially 15v voltage is regulated and 10V is supplied to one of the op-amp terminals,ensuring a constant output voltage of 10V. The op amp is supplied with 15V and 0V to ensure that positive voltage is fed back to the Darlington. In order to further regulate the voltage to the desired level of 12V, a Zener diode is implemented.

#### Current regulation
TIP142 Darlington pair is utilized to control the current. The op-amp provides feedback to the Darlington pair and by using that control the current. Here, the Darlington pair work as a current controlling gate.

### Current Limiting
This power supply is required to limit the maximum current up to 10A. When the current through a circuit exceeds its rated current, it may cause overheating, and component failure.Thus,implementinganovercurrentprotection circuit, prevent damage to the device and ensures proper functionality. There are many techniques to implement current limiting circuit. The use of a relay is 
a common practice. In such circuits, changeover contacts are utilized to connect the supply voltage when the current is lower than the rated current and to open the contact when the current exceeded the rated 
current. Two spdt relays are utilized in this design. Since normally open contact points are used, current must be allowed to flow through the coil so that the contacts remain closed. To address this, an NPN transistor (Q1) is added in series with the coil, along with a 1k resistor (R6)between the supply voltage and the base of the transistor. When voltage is applied to the circuit, current flows through the base-emitter path of the transistor and causes it to operate in the saturated region. As a result, the coil of both relays areenergized, and the contact is closed. A flyback diode is added to prevent the occurrence of huge voltage spikes when the relay coil is deenergized. A green LED is used to indicate the absence of over current problem. 

### Protection

The final stage is protection which includes circuit protection mechanisms.

## Conclusion

This project was finalized with two PCB and a 3D-printed enclosure to house the PCB. The power supply was successfully able to drive a high-power load (100W) from a 230V input voltage.
