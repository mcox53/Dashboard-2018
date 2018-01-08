The purpose of this file is to create and test code to configure the USART line on the ATmega328p to be used as a Master/Slave SPI interface.

According to the ATmega328p datasheet section 25.2:

"The Universal Synchronous and Asynchronous serial Receiver and Transmitter (USART) can be set to a
master SPI compliant mode of operation.
Setting both UMSELn[1:0] bits to one enables the USART in MSPIM logic. In this mode of operation the
SPI master control logic takes direct control over the USART resources. These resources include the
transmitter and receiver shift register and buffers, and the baud rate generator. The parity generator and
checker, the data and clock recovery logic, and the RX and TX control logic is disabled. The USART RX
and TX control logic is replaced by a common SPI transfer control logic. However, the pin control logic
and interrupt generation logic is identical in both modes of operation.
The I/O register locations are the same in both modes. However, some of the functionality of the control
registers changes when using MSPIM."

The goal here being to utilize this second line for less critical applications and possibly utilize more devices.
