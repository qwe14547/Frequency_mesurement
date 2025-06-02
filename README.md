# Digital Frequency Counter using IC 4026, 4013, and 4060

This project implements a simple digital frequency counter using basic CMOS ICs and a 7-segment display. It is designed to measure the frequency of an input pulse signal using a gated time window of 1 second.

## 📌 Overview

The frequency counter measures incoming pulses and displays the count on three 7-segment displays. The counting interval is controlled using a crystal oscillator-based timing circuit, enabling accurate and automatic 1-second measurement windows.

## ⚙️ Components Used

- **IC 4026** × 3 – Decade counter with 7-segment decoder/driver  
- **IC 4013** × 2 – Dual D-type flip-flops (for frequency division and control logic)  
- **IC 4060** × 1 – Oscillator and frequency divider (1 Hz generation using crystal)  
- **Crystal Oscillator** – For generating stable time base  
- **7-Segment Displays** × 3  
- **Resistors** – 220Ω, 330kΩ  
- **AND Gate IC** – For gating control  
- **Power Supply** – 5V/9V  
- **Breadboard / PCB** and connecting wires  

## 🔍 Working Principle

1. **Clock Generation:**  
   IC 4060 with a crystal oscillator generates a 1 Hz signal. A D flip-flop (IC 4013) divides it further to get a 0.5 Hz square wave (2-second period).

2. **Gating Logic:**  
   A second flip-flop is used to gate the input signal for 1 second using the 0.5 Hz clock. This allows counting during the HIGH phase and stopping afterward.

3. **Counting Pulses:**  
   During the 1-second gate interval, the input pulses are passed through an AND gate to the clock input of IC 4026 counters, which drive the 7-segment displays.

4. **Display:**  
   The final output is shown as a 3-digit frequency reading, directly indicating the number of pulses received in 1 second (i.e., the input signal frequency in Hz).

## ✅ Features

- Fully hardware-based frequency counter  
- Real-time frequency display using 7-segment LEDs  
- Accurate timing using crystal oscillator  
- No microcontroller or programming required  
- Simple, low-cost, and easily replicable design  

## 🛠 Applications

- Lab signal testing  
- Signal frequency measurement  
- Educational electronics projects  
- DIY electronics tools  

## 📄 Authors

- **Shreyansh Rastogi**  
- **Nishita Patel**  
- **Yash Kharche**  

> This project was developed as part of the *Digital Circuits* coursework at VNIT Nagpur.


