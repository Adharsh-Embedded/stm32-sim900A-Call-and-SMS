# STM32 SIM900A SMS and Call Alert System

## Overview

This project demonstrates how to interface a SIM900A GSM module with the STM32 Nucleo-F446RE using UART communication. The system can send SMS messages and make phone calls using AT commands. A push button is used to trigger the alert sequence.

## Hardware Used

* STM32 Nucleo-F446RE
* SIM900A GSM Module
* Push Button
* SIM Card
* External 5V Power Supply

## Connections

| SIM900A | STM32              |
| ------- | ------------------ |
| TXD     | USART1_RX          |
| RXD     | USART1_TX          |
| GND     | GND                |
| VCC     | External 5V Supply |

## Features

* Send SMS alerts
* Make emergency phone calls
* UART communication using AT commands
* Button-triggered operation

## AT Commands Used

### Send SMS

```text
AT+CMGF=1
AT+CMGS="+91XXXXXXXXXX"
Message Text
Ctrl+Z
```

### Make Call

```text
ATD+91XXXXXXXXXX;
```

### Hang Up

```text
ATH
```

## Project Workflow

1. Press the push button.
2. STM32 sends an SMS alert to the predefined number.
3. The system waits for SMS transmission to complete.
4. STM32 initiates a phone call to the same number.

## Challenges Faced

* Understanding GSM AT commands
* Handling delays between SMS and call operations
* Configuring UART communication correctly
* Debugging SIM900A network and call behavior

## Future Improvements

* MPU6050 Fall Detection Integration
* GPS Location Tracking
* SMS Delivery Confirmation
* Incoming Call Handling
* Interrupt-Based Button Detection
* FreeRTOS Integration

## Author

**Adharsh**

## Development Environment

* Board: STM32 Nucleo-F446RE
* Language: Embedded C
* IDE: STM32CubeIDE
* Communication Protocol: UART
