# Renesas-RA6M4_USB_CDC


## 1. Project Overview:
This project demonstrates the basic functionality of the USB PCDC driver on Renesas RA MCUs based on Renesas FSP using FreeRTOS. In this example, the user will be able to use the RA board as a  CDC to UART converter by connecting through a COM port from the host PC. The converter performs the data reception and data transmission asynchronously. The user can connect any UART device to receive the data typed in Tera Term, and to send any data to the converter to display on Tera Term. The user can also change the baud rate, stop bit and parity bit configuration at run time through Tera Term. The status of the application will be displayed on JLink RTT Viewer.

## 2. Hardware and Software Requirements:

Hardware : 
   
1) RA board 
 
2) 2x Micro USB device cable
   
3) A PC with at least 2 USB port(1 for debug and 1 for COM port)
   
4) Connecting/Jumper wires for shorting pins   
    
Software: 

1) Serial Terminal(TeraTerm)
   
2) Windows® 10 operating system
 
3) USB Serial Drivers (included in Windows 10)
  
4) Jlink RTT viewer

## 3. Hardware settings for the project:
   
Jumper Settings:

EK-RA6M3 :

USB PCDC (High Speed):

1. Jumper J7: Connect pins 2-3

2. Connect Jumper J17 pins

3. Connect the micro USB end of the micro USB device cable to micro-AB USB High Speed port (J6) of the board.  Connect the other end of this cable to USB port of the host PC.

USB PCDC (Full Speed):

1. Jumper J12: Connect pins 2-3

2. Connect Jumper J15 pins

3. Connect the micro USB end of the micro USB device cable to micro-AB USB Full Speed port (J11) of the board.  Connect the other end of this cable to USB port of the host PC.
	
UART:

1. p411 (TXD) to RX pin of external UART device

2. p410 (RXD) to TX pin of external UART device

3. When using flow control from TeraTerm, the CTS (P413) should be connected to either RTS(P103) or GND. For instructions on how to enable and disable flow control, refer the the FSP User's manual. 

EK-RA4M2:

USB PCDC (Full Speed):

1. Connect the micro USB end of the micro USB device cable to micro-AB USB Full Speed port (J11) of the board.  Connect the other end of this cable to USB port of the host PC.

2. Jumper J12 placement is pins 2-3

3. Connect jumper J15 pins

UART:

1. p602 (TXD) to RX pin of external UART device

2. p601 (RXD) to TX pin of external UART device

3. When using flow control from TeraTerm, the CTS (P603) should be connected to GND. For instructions on how to enable and disable flow control, refer the the FSP User's manual.

EK-RA6M4:

USB PCDC (Full Speed):
	    
1. Connect the micro USB end of the micro USB device cable to micro-AB USB Full Speed port (J11) of the board.  Connect the other end of this cable to USB port of the host PC.

2. Jumper J12 placement is pins 2-3
  
3. Connect jumper J15 pins

UART:

1. p101 (TXD) to RX pin of external UART device

2. p100 (RXD) to TX pin of external UART device

3. When using flow control from TeraTerm, the CTS (P414) should be connected to P413.
               For instructions on how to enable and disable flow control, refer the the FSP User's manual.

        	
Note:

1. The user can connect any other UART device to communicate with the USB PCDC to UART converter.
   
2. To enable testing of the converter, the user can also loop back the TX and RX pins on the EK-RA6M3 USB to UART converter.
   
3. High-speed is supported the default configuration setting in the project for MCUs which support high-speed USB.
   For MCU with full speed USB only, full speed USB will be default configuration setting. For switching from High-speed to full-speed,
   refer instructions in the README.md.


