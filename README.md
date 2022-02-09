# D_level_triggered_FF

 This Project  implements the design of level triggered D Flip Flop with CMOS logic using eSim (an open-source Electronic Design Automation tool designed by FOSSEE Project team of Indian Institute of Technology Bombay) and SkyWater 180nm PDKs (Process Design Kit) sponsored by Google.

## Table of Contents

- [Introduction](#introduction)
- [Description](#description)
- [Reference Circuit Diagram](#reference-circuit-diagram)
- [eSim EDA Tool](#esim-eda-tool)
- [Google SkyWater PDK](#google-skywater-pdk)
- [Schematic Diagram](#schematic-diagram)
- [Write Opearation](#write-operation)
- [Read Operation](#read-operation)
- [Steps to Reproduce waveforms](#steps-to-reproduce-waveforms)
- [References](#references)
- [Acknowledgement](#acknowledgement)
- [Author](#author)

## Introduction

The most important memory element in a sequential  logic circuit is Flip-Flop. A flip flop is a bistable multivibrator which has two stable states. It can have one or more  inputs, which helps the device to flip and flop between the possible output states. It  can store one bit of data either 0 or a 1. They are  classified as SR Flip-Flop, D Flip-Flop, JK Flip- Flop and T Flip-Flop. These flip flops are used  in building registers and counters. The proposed paper shows the implementation of level triggered D Flip-Flop using CMOS with 130nm SkyWater technology. 


## Reference Circuit Diagram


![20220209_215238](https://user-images.githubusercontent.com/74066861/153244008-cc7f9a6a-6bf5-4095-908e-9a7472d490fe.jpg)


## Description

In an SR flip flop, the condition S=R=1 generating invalid state is undesirable. To avoid this condition, a not gate is placed between the S and R inputs. The 
result is SR flip flop is converted into a D flip-flop (data flip-flop or delay flip-flop). Here, the data is fed at the D input. The circuit consists of 3 PMOS and 3 NMOS transistors. When CLK=1 and D=0 ,VGS for M1 is +ve and hence M1 is on which in turn short circuits the source and drain terminals of M1. As a result, source of M1 will be at 0 level and gate of M2 will be at 5V as CLK=1 due to which VGS for M2 is +ve thereby M2 will be in off state. Hence input to CMOS inverter consisting of M3 and M4 is 0, therefore M3 will be in on state and M4 will be in off state thereby Qbar =1. This in turn turns off M5 and turns on M6, hence final output Q = 0. Similarlycircuit can be verified for other combinations.



## eSim EDA Tool
eSim is an open source EDA tool for circuit design, simulation, analysis and PCB design, developed by FOSSEE Team at IIT Bombay. It is an integrated tool build using open source softwares such as KiCad, Ngspice and GHDL.



![Screenshot (148)](https://user-images.githubusercontent.com/74066861/153248249-3b0c7f1d-6da2-4569-871d-644044b9a982.png)







## Schematic Diagram

![final_dff_page-0001](https://user-images.githubusercontent.com/74066861/153242896-ac11ebab-2164-472c-a756-e2bf5b24c834.jpg)


Spice Netlist generated by eSim for the above schematic using 180nm library for MOSFETs.

![netlist](https://user-images.githubusercontent.com/74066861/153246037-94ea6733-b970-4388-8779-4dd371702051.PNG)



## Simulation Details





## Ngspice Waveform


![ngspice_final](https://user-images.githubusercontent.com/74066861/153246947-767a2817-7f01-4db1-bf23-621628b6a3e7.PNG)


![final_waveform_d](https://user-images.githubusercontent.com/74066861/153246627-0a0fdb3a-92e0-4605-84c4-533f4a4b66cf.PNG)







## Acknowledgement

[Kunal Ghosh](https://github.com/kunalg123), Co-founder of VLSI System Design (VSD) Corp. Pvt. Ltd.


## Author

[Parthiv Kamath CS](https://github.com/Parthiv-2020), 3rd  Year  B.E. in Electronics and Communication Engineering
- Contact: parthivkmth5@gmail.com
