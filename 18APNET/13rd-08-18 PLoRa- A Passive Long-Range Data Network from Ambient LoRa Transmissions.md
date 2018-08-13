# PLoRa: A Passive Long-Range Data Network from Ambient LoRa Transmissions
* [Yao Peng] 
* [Keywords: Backscatter, LoRa, Low-power, Long-range]

## Abstract

> ### 1.Contribution
> <b>This paper presents PLoRa, an ambient backsactter design that enables long-range wireless connectivity for batteryless IoT devices</b>. PLoRa takes ambient LoRa transmissions as the excitation signals, conveys data by modulating an excitation signal into a new standard LoRa "chrip" signal, and shifts this new signal to a different LoRa channel to be received at a gateway faraway.
> 
> PLoRa achieves this by a holistic RF front-end hardware and software design, including a low-power packet detection circuit, a blind chirp modulation algorithm and a low-power energy management circuit. 
> 
> Also intergrate a light-weight backsactter signal decoding algorithm with a MAC-layer protocol that work together to make coexistence of PLoRa tags and active LoRa nodes possible in the network.
> 
> We prototype PLoRa on a 4 later printed circuit board and test it in various outdoor and indoor environments.

---

## Introduction

> Next generation envisions ubiquitous, cheap, and low data-rate connectivity among humans machines, and objects. such wireless communication should satisfy the following three requriements.
>
> * (1) Battery-free
> 
> * (2) Long-range
> 
> * (3) Ambient excitation signal
>
> No existing wireless technology satisfy all three requriements. 
> 
> This observation leads us to propose PLoRa, a Passive LoRa communication techonolog that enables long-raneg connectivity for IoT devices based on ambient excitation, without the need for a dedicated excitation source.
> 
> PLoRa can communicate with both active LoRa nodes and gateways over long distances in three distinct ways(as also shown in Figure 1):
> 
> * (a) Conventional backsactter 
> 
> * (b) Opportunistic uplink piggybacking 
> 
> * (c) Opportunistic downlink piggybacking

---

### Hard Parts
> * [1].First: since the PLoRa tag is battery-free, it should consume an ultra-low amount of power during which it is idle.
> 
> * [2].Second: unlike the sinusoidal tone used in RFID and most other backscatter systems , the excitation signal in PLoRa is the normal downlink and uplink LoRa chirps that convey data and change over time.
> 
> * [3].Third: given the large energy demands of the computational and communication tasks, the battery-free PLoRa tag will soon drain its energy and stop working, which will cause complete loss of data stored in its volatile memory.
> 
> * [4].Apart Also propose a light-weight backsactter signal decoding algorithm and a MAC-layer protocol to facilitate the coexistence of PLoRa tags and commercial active LoRa nodes in a loRaWAN.
---

### *Contributions* 

<b> • Proposing a holistic hardware-software co-design to achieve low-power long-range backscatter communication.</b>

<b> •Implementing this hardware-software co-design on the PCB board and evaluating its performance through a long-term (three months) experiment in both indoor and outdoor environment.</b>
Limitations.

### *Limitations*

<b>• PLoRa’s packet detection range is limited to 50 m </b>

<b>• the current PLoRa design encodes one bit per LoRa symbol and thus achieves a low data rate </b>


