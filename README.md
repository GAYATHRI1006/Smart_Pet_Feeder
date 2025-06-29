# Automatic Pet Feeder

An Arduino-based smart pet feeder system that uses a real-time clock (DS3231), servo motor, 16x2 LCD, and keypad to schedule pet feeding times and automate the feeding process.

## Developed By
**Gayathri G**  
GitHub: [GAYATHRI1006](https://github.com/GAYATHRI1006)
## Screenshot
![Smart Pet Feeder Screenshot](image.png)

## Features

- **Time-Based Feeding**: Set feeding times using a keypad.
- **RTC Module (DS3231)**: Keeps accurate time even after power loss.
- **Servo Motor Operation**: Dispenses food at the scheduled time.
- **LCD Display**: Shows current time and date.
- **Manual Time Setting**: Pressing a button allows users to configure feeding time interactively.

## Components Used

| Component            | Description                          |
|----------------------|--------------------------------------|
| Arduino UNO/Nano     | Microcontroller                      |
| DS3231 RTC Module    | Real-Time Clock                      |
| 16x2 LCD Display     | For showing time and status          |
| 4x4 Matrix Keypad    | For inputting feeding time           |
| Servo Motor          | Controls food dispensing mechanism   |
| Push Button          | To enter time-setting mode           |
| Jumper Wires, Breadboard | For circuit connections         |

## Pin Connections

| Module       | Arduino Pins     |
|--------------|------------------|
| Keypad Rows  | D2–D5            |
| Keypad Cols  | D6–D9            |
| RTC (DS3231) | SDA – A4, SCL – A5 |
| Servo Motor  | D10              |
| LCD Display  | RS–A0, EN–A1, D4–A2, D5–11, D6–12, D7–13 |
| Button       | A3               |

## How It Works

1. On boot, the current time and date are displayed using the RTC module.
2. Pressing the push button (`A3`) enters feeding time setting mode via keypad.
3. User inputs time in `HH:MM` format using keypad.
4. When real-time matches the set time, the servo motor rotates to dispense food.
5. Feeding only happens once per scheduled time; resets when new time is set.

## Usage Instructions

1. Connect all components as per the wiring table.
2. Upload the code to Arduino.
3. Monitor serial output for debugging (optional).
4. Press the button to set the feeding time.
5. Wait for the feeder to activate at the scheduled time.

## Safety Notes

- Ensure servo rotation is not obstructed.
- Use external power supply if servo draws too much current.

