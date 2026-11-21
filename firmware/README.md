# Firmware

The firmware folder is reserved for the ESP32 program.

The planned firmware will:
- Read the capacitive soil moisture sensor.
- Read temperature from the DS18B20 probe.
- Read the pH interface output after the pH hardware is finalized.
- Show basic readings and status on the OLED.
- Give local LED or buzzer alerts.
- Send sensor readings to the phone using Bluetooth Low Energy (BLE).

No working firmware has been uploaded here yet. The ESP32 board is still awaiting delivery, and the pin mapping must be finalized before writing and testing the full program.

The AI crop identification, plant image scanning and Soil Health Card / NPK report scanning are planned phone-app features. They are not performed by the ESP32 firmware or measured directly by the current sensor board.
