# USB-C Power Delivery Implementation

## Overview
This project is part of my thesis on embedded systems and power management, focusing on the implementation of USB-C Power Delivery (USB-C PD) using C programming. The goal is to develop an embedded system capable of negotiating power contracts between a USB-C power source and a power sink device.

## Features

- **USB-PD Communication**: Handles power negotiation via Configuration Channel (CC) lines.
- **Dynamic Power Selection**: Supports three voltage modes:
  - **5V Mode**
  - **9V Mode**
  - **12V Mode**
- The user can select the desired voltage using the joystick on the STM32G474. Upon selection, the system requests the corresponding voltage, and an LED indicator confirms the selection when negotiation is successful.
- **Real-time Monitoring**: Logs power delivery status, including voltage, current, and contract negotiation.
- **Safety Mechanisms**: Implements protections against overvoltage, undervoltage, and excessive current draw.

## Hardware Requirements

- STM32G474 microcontroller
- USB-C power source (charger or power adapter)
- USB-C sink device (custom board or test device)
- Joystick for voltage selection
- LED indicators for confirmation

## Software Components

- Embedded firmware handling USB-PD communication
- Event-driven architecture for power contract negotiation based on joystick input
- Low-level CC line interaction to determine source/sink roles

## Installation & Usage

### 1. Clone the Repository
```sh
git clone https://github.com/yourusername/usb-c-pd.git
cd usb-c-pd
```

### 2. Compile the Firmware
Ensure you have a compatible ARM GCC toolchain installed.
```sh
make
```

### 3. Flash the Microcontroller
Use STM32CubeProgrammer or OpenOCD to upload the firmware:
```sh
st-flash write firmware.bin 0x8000000
```

### 4. Select Power Mode
- Use the joystick on the STM32G474 to request **5V, 9V, or 12V**.
- The system sends a USB-PD request to the power source.
- If the negotiation is successful, the corresponding **LED indicator** lights up.

### 5. Monitor Power Negotiation
- Use a **USB analyzer** or **serial output** to track power contract exchange.
- Logs are available via **UART** for debugging.

## Future Improvements

✅ **Integration with Programmable APDO** – Support for adjustable voltage/current profiles.
✅ **Enhanced Debugging & Logging** – Improved real-time tracing for power negotiation.
✅ **Graphical Monitoring UI** – A web-based dashboard for live power monitoring.

## Contributing
Pull requests are welcome! For major changes, please open an **issue** first to discuss your ideas.

## License
This project is licensed under the **MIT License**.

## Author
This project was developed as part of my thesis on **USB Power Delivery** and **embedded systems**.

For more details or inquiries, feel free to **contact me**!
