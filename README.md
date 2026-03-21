# Warble

Retro-Logic LED Matrix Controller Powered by TinyS3 & Adafruit Matrix Bonnet
This project adapts a TinyS3 (ESP32-S3) microcontroller to drive a 32x16 RGB LED Matrix using an Adafruit RGB Matrix Bonnet as a high-quality 5V logic level shifter and power distribution. By bypassing the Raspberry Pi, we achieve near-instant boot times and rock-solid DMA-driven animations.

## Hardware Components
- Microcontroller: Unexpected Maker TinyS3 (ESP32-S3)
- Display: Adafruit 32x16 RGB LED Matrix (6mm pitch)
- Interface/Buffer: Adafruit RGB Matrix Bonnet for Raspberry Pi
- Power: 5V 4A External DC Power Supply (Connected via Bonnet DC Jack)
- Connectivity: Female-to-Male Jumper Wires (to bridge TinyS3 to Bonnet Header)

## Wiring Map (TinyS3 to Bonnet Header)
Since we are repurposing the 40-pin Raspberry Pi header on the Bonnet, use the following mapping to connect the TinyS3 GPIOs.

> Note: Pin 1 on the Bonnet header is typically marked with a square pad or a "1". Even pins are on one row, odd on the other.

| Matrix Signal | Bonnet Pin (Physical #) | TinyS3 GPIO | Note |
| :--- | :--- | :--- | :--- |
| **R1** | Pin 29 | **GPIO 1**   | orange |
| **G1** | Pin 33 | **GPIO 2**   | green  |
| **B1** | Pin 31 | **GPIO 3**   | blue   |
| **R2** | Pin 32 | **GPIO 4**   | red    |  
| **G2** | Pin 36 | **GPIO 5**   | white  |
| **B2** | Pin 16 | **GPIO 6**   | white  |
| **A** | Pin 15 | **GPIO 7**    | purple |
| **B** | Pin 37 | **GPIO 8**    | yellow |
| **C** | Pin 13 | **GPIO 9**    | grey   |
| **LAT** | Pin 7 | **GPIO 11**  | green  |
| **OE** | Pin 12 | **GPIO 12**  | yellow |
| **CLK** | Pin 11 | **GPIO 13** | red    |
| **GND** | Pin 6 | **GND**      | black  |