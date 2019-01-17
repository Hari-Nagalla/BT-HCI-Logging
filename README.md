 
# BT-HCI-Logging
These HCI sniffer tools capture HCI traffic between a host and controller in a two processor architecture and saves the logs in BT Snoop format.

The usage is as follows (These are java based tools. So, make sure JRE (Java Runtime Environment) is installed on the PC.)

a) hcisniffer.jar
Tap the UART lines (H4) between the Host and controller for sniffing. Use a suitable UART-USB adapter to connect to a PC. On the PC, you would see would see two UART ports, one for HCI/UART Tx line and another for HCI/UART Rx lines being sniffed.

c:\hci-tools\java -jar hcisniffer.jar <COM Port#1> <COM Port#2> <hci baud rate#> <bt-snoop logfile#>

b) swosniffer.jar
This tool is intended to work with ARM Cortex-M devices with ITM/DWT/SWO CoreSight features. Configure the Cortex-M for data tracing of HCI UART read, writes. The SWO out put data is read through a UART/USB adapter to the PC.

c:\hci-tools\java -jar swosniffer.jar <COM Port#> <SWO baudrate#> <bt-snoop logfile#>

END
