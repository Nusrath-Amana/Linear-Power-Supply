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

The third stage is regulation which maintains the constant output voltage.

### Protection

The final stage is protection which includes circuit protection mechanisms.

## Conclusion

This project was finalized with two PCB and a 3D-printed enclosure to house the PCB. The power supply was successfully able to drive a high-power load (100W) from a 230V input voltage.
