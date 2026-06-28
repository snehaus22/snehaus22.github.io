---
layout: post
title: EMG-Controlled Prosthetic Hand
description:  A myoelectric prosthetic hand that uses forearm muscle signals to control grasp motions. A prosthetic control system that captures EMG signals from forearm muscles using surface electrodes. These signals were amplified, filtered, and processed through a microcontroller(Arduino NanoEvery) to distinguish intentional muscle activation from noise and convert the incoming analog signal to a digital output. If above the set threshold, the motors activated, causing the 3D-printed hand to contract. I focused heavily on circuit desing, signal conditioning, thresholding, and safety considerations to ensure reliable control.
skills: 
- Arduino NanoEvery Firmware
- Signal Filtering
- Circuit Safety
- 3D Printing
- CAD
main-image: /EMGcontrolledhand.png
---

# Design Specs
- Design must replicate the function of a hand
- Tests: Object hold, sustained grip, repeated grip

- Design must be functional without the presence of a hand
- Test: General finger flexion in response to EMG

- Design components should not interfere with function
- Test: General flexion and object hold

- Design must be sensitive enough to function at low forearm muscle activity
- Test: Grip strength test
<br>

## Schematic & PCB 

{% include image-gallery.html images="armschematic.png" height="400" %} 
{% include image-gallery.html images="armpcb.png" height="400" %}
<br>

## Fully Assembled 3D Printed Hand

{% include image-gallery.html images="robotichand.png" height="400" %} 
<br>

## Firmware
- ADC conversion: 0-5 V mapping to 0-1023 
- High threshold of 3 V
- Low threshold of 2.5 V for hysteresis
- Once above the high threshold, motors activated
- Once below the low threshold, motors stopped
- Input signal to analog pins, digital pins to MOSFET
