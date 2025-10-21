# Smart Thermostat - Raspberry Pi

This project demonstrates a smart thermostat implemented on a Raspberry Pi using Python. The thermostat uses a state machine to manage three modes: off, heat, and cool. The system interacts with LEDs, buttons, an LCD display, and a temperature sensor to simulate real-world behavior.

Additionally, a Thermostat Server Simulator can receive and display status updates sent from the thermostat over the serial port.

---

## Features

- Three thermostat states:
  - Off – no LEDs lit
  - Heat – Red LED fades when heating is required
  - Cool – Blue LED fades when cooling is required

- Buttons:
  - Cycle between modes
  - Increase or decrease temperature setpoint

- LCD Display:
  - Line 1: Current date and time
  - Line 2: Alternates between current temperature and thermostat state/setpoint

- Serial Output:
  - Thermostat sends a status update every 30 seconds (state,current_temp,setpoint)
  - Thermostat Server Simulator reads and prints this data

---

## State Machine

The thermostat is powered by a Python state machine, which controls:
- Transitions between off, heat, and cool
- LED behaviors for visual feedback

---

## Dependencies

- Python 3
- Raspberry Pi GPIO libraries
- Hardware: Raspberry Pi, AHT10/AHT20 temperature sensor, 16x2 LCD, 3 LEDs, 3 buttons

---

## Usage
1. Clone the repository
2. Install dependencies
3. Run the thermostat
4. Use the buttons to cycle states and adjust the setpoint. The LCD and LEDs reflect current status
