---
layout: page
title: Characterization of 8-bit Flash ADC for CMOS Image Sensor Readout
description: A 4 MS/s 8-bit Flash ADC in 180 nm CMOS with full IEEE 1241 characterization
img: assets/img/projects/frankie-thesis-thumbnail.png
importance: 1
category: Master's Thesis 
selected: true
related_publications: true
---

The rapid scaling of global semiconductor manufacturing has made device characterization an essential pillar of modern supply chains. Among the most ubiquitous mixed-signal building blocks, the analog-to-digital converter (ADC) demands rigorous performance validation to ensure the reliability of the systems that rely on it.

## Architecture

This work presents a 4 MS/s 8-bit Flash ADC fabricated in a standard 180 nm CMOS process, designed as a readout converter for a CMOS image sensor. Two identical ADC instances serve even and odd pixel columns respectively, providing the imager with a frame rate of approximately 40 FPS.

The architecture follows the standard Flash topology:

- **Sample & Hold** — slew rate of ~3.6 V/µs
- **Comparator** — pre-charged PMOS input with latch structure
- **Encoder** — typical one-hot ROM

{% include figure.liquid
   path="assets/img/projects/flash_adc_arch.jpg"
   caption="Block diagram of the Flash ADC architecture."
   class="img-fluid rounded z-depth-1" %}

## Characterization

Device characterization strictly follows the **IEEE 1241** standard for ADC testing, utilizing standard laboratory equipment, Verilog control logic on a custom PCB, and a Python GUI for automatic data acquisition and processing.

### Static Performance

| Metric | Result |
| --- | --- |
| Peak DNL | +3.15 / -1.0 LSB |
| Peak INL | +2.68 / -3.19 LSB |

{% include figure.liquid
   path="assets/img/projects/flash_adc_dnl_inl.jpg"
   caption="Measured DNL and INL across the full ADC transfer curve."
   class="img-fluid rounded z-depth-1" %}

### Dynamic Performance at 4 MS/s

| Metric | Result |
| --- | --- |
| SINAD | 31.52 dB |
| THD | -32.9 dBFS |
| ENOB | 4.94 bits |

{% include figure.liquid
   path="assets/img/projects/flash_adc_fft.jpg"
   caption="Output spectrum showing SINAD and THD at 4 MS/s."
   class="img-fluid rounded z-depth-1" %}

## Test Framework

Beyond ADC characterization, this work establishes a reusable test framework and documented procedure to support future integrated circuit validation efforts at the WPI CHIPS Design Studio.

## Publications

{% cite 10658797 %}
