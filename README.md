README – USB-C Power Delivery Implementation

Overview

This project is the result of my thesis, focusing on the implementation and management of USB-C Power Delivery (USB-C PD) using C programming. The goal was to develop an embedded system capable of negotiating power contracts between a USB-C power source and a power sink device.

Features

USB-PD Communication: Implements communication between source and sink devices via Configuration Channel (CC) lines.

Power Negotiation: Supports different power profiles, enabling dynamic voltage and current selection based on device requirements.

Three Power Modes:

5V Mode

9V Mode

11V Mode
The voltage selection is controlled by the joystick of the STM32G474. Depending on the button pressed, the system requests the corresponding voltage level from the power source. Upon successful negotiation, the system provides visual confirmation using an LED, which lights up to indicate the selected mode.


Real-time Monitoring: Provides feedback on power delivery status, including voltage, current, and negotiation outcomes.

Error Handling & Safety Mechanisms: Ensures safe power exchange by monitoring conditions such as overvoltage, undervoltage, and excessive current draw.


Technical Details

Programming Language: C

Protocol: USB Power Delivery (USB-PD)

Hardware Requirements:

STM32G474 microcontroller

USB-C power source (charger or power adapter)

USB-C sink device (custom board or test device)

Joystick for voltage selection

LED indicators for confirmation


Software Components:

Embedded firmware handling USB-PD communication

Low-level interaction with CC lines for power role identification

Event-driven architecture for power contract negotiation based on joystick input



Installation & Usage

1. Compile the Firmware:

Use a compatible toolchain (e.g., GCC for ARM if using an STM32 microcontroller).



2. Flash the Microcontroller:

Upload the compiled firmware to the microcontroller using an appropriate flashing tool.



3. Select the Power Mode:

Use the joystick on the STM32G474 to request 5V, 9V, or 11V from the power source.



4. Verify the Power Selection:

Check the corresponding LED indicator, which lights up to confirm the selected voltage mode.



5. Monitor Power Negotiation:

Use a USB analyzer or serial output to track the power contract exchange.




Future Improvements

Integration with Programmable APDO: Support for adjustable voltage and current profiles.

Enhanced Debugging & Logging: Improved real-time tracing for debugging power negotiation.

Graphical Interface for Monitoring: Development of a UI for visualizing power exchange in real time.


Author

This project was developed as part of my thesis in embedded systems and power management. It provides a foundation for further research and development in USB Power Delivery technology.

For more details or inquiries, feel free to reach out!

# PowerDeliveryProject