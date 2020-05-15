# STM32F4_LIDAR
 
1. Description

Lidar sensor VL53L0X, working on STM32F4 Discovery. A small, ported API library is attached : VL53L0X.c, VL53L0X.h and I2CDev.h which must be found also in the Src and respectively Inc directories.
The distance is continuously read by the sensor, and every 500 ms the values in mm are sent with UART1 115200/n/8/1 to a standard terminal, which displays it. 

2. How to use

Dowload the whole content of the project.
Run the CubeMX file LIDAR.ioc and generate project for IAR EWARM. Open the generated project, Download and Degug (Ctrl+R) in the Master board, then Go (F5).
In the Live watch field in IAR we may see the distance. 

3. Software context

The project was verified using:

-STM32 Cube MX version 5.6.0

-Firmware package STM32Cube FW_F4 V1.25.0

-IAR-EWARM v 8.50.1.

-The attached API library VL53L0X.c, VL53L0X.h and I2CDev.h are placed in the Src and respectively Inc directories.

Notice: For other software context, some modifications may be necessary, as the future evolution of these products is unknown.

4. Hardware context

-STM32F4 -Discovery, as with USART1 on PB6 and PB7, and I2c on PB8 and PB9.

-VL53L0X module on I2C1 with GND and VIN coupled to GND and VCC.

-CH340  TTL to USB adapter on Master

5. Youtube classroom: https://www.youtube.com/watch?v=b2w9nrRq9nw
