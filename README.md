# Temp_Sensor

This project reads ambient temperature using a TMP36 analog temperature sensor and displays the temperature (in °C) on a 16x2 LCD screen using an Arduino Uno. The project demonstrates the use of analog sensors, LCD interfacing, and data conversion for real-time monitoring.

## Components Used:

Arduino UNO
TMP36 Temperature Sensor
16x2 LCD Display (with potentiometer for contrast control)
10kΩ Potentiometer
220Ω Resistor (for LCD backlight)
Jumper Wires
Breadboard

## Circuit Connections:

Component	Arduino Pin
TMP36 VCC	5V
TMP36 GND	GND
TMP36 OUT	A0 (Analog Input)
LCD RS	D12
LCD EN	D11
LCD D4–D7	D5, D4, D3, D2
LCD VSS, RW, K	GND
LCD VDD, A	5V
Potentiometer	Middle pin to V0 (LCD contrast), sides to 5V and GND

## How It Works:

The TMP36 sensor outputs an analog voltage based on ambient temperature.
Arduino reads this analog value via A0.
The temperature is calculated using the TMP36 formula:
Temp (°C) = (analogValue × 5.0 / 1024.0 – 0.5) × 100
The result is displayed on the LCD screen in real-time.
