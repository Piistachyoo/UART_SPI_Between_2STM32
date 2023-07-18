
# UART_SPI_Between_2STM32

This project consists of 2 STM32F103, connected with SPI protocol

MCU1 is master in the spi connection, and we will send data on its UART using a terminal

MCU2 is slave in the SPI connection, and we will read the sent data from MCU1 on its UART output
### The flow of data is:
##### Terminal -> UART(MCU1) -> SPI (MCU1->MCU2) -> UART(MCU2) -> Terminal
1. User sends a character on MCU's terminal
2. MCU1 generates an interrupt when a character is received on UART, and sends the character to MCU2 using SPI protocol
3. MCU2 generates an interrupt when data is received from SPI protocol, and receives the character to display it on the terminal using UART
4. Sent character is shown for user on MCU2's terminal

## Simulation:

![enter image description here](https://github.com/Piistachyoo/UART_SPI_Between_2STM32/blob/main/simulation.gif?raw=true)