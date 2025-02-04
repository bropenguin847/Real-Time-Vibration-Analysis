# Real-Time-Vibration-Analysis
Using STM32 Black Pill with MPU 6050 accelerator sensor

## Introduction
his project focuses on developing a real-time vibration analysis system using the STM32F411CEU6 microcontroller (Black Pill) and the MPU6050 sensor, integrated through I2C communication. The MPU6050 combines a 3-axis accelerometer and a 3-axis gyroscope, providing motion and vibration data for analysis. Data acquisition and processing were implemented using STM32CubeIDE, with results displayed in Serial Studio for visualization. The system serves practical applications such as detecting vibrations in machinery, monitoring structural integrity, or analyzing dynamic motions in robotics and vehicles.

## Wiring Diagram
<img src="images\Wiring Diagram.png" alt="Wiring Diagram">

## Components
<kbd>
<img src="images\BOM.png" alt="BOM">
</kbd>
  
## Steps
1. Download necessary softwares: STM32CubeIDE
   * Go the [ST official website](https://www.st.com/en/development-tools/stm32cubeide.html). When downloading this for the first time, users need to manually create a MyST account with their email. After that, the download link will be sent to the email inbox. Simply click the link, and the download will start automatically.
   * <kbd><img src="images\downloadStm32.png" alt="downloadStm32"></kbd>

---

2. Manually setup STM32 blackpill (STM32F411CEU6) in STM32CubeIDE.
    1. Click on "Create a New STM32 project", enter "STM32F411CEU6" in Commercial Part Number. And select it MCUs/MPUs List.
      - <kbd><img src="images\selectBlackPill.png" alt="selectBlackPill"></kbd>
    2. Enter any project name, and then select the file location. After that, click Finish.
    3. Go to Clock Configurations tab and configure the settings as below:
      - <kbd><img src="images\clockConfig.png" alt="clockConfig"></kbd>
    4. Go to Pinout & Configurations tab and configure the settings as below:
       - At System core:
       - <kbd><img src="images\sys.png" alt="sys"></kbd>
       - <kbd><img src="images\rcc.png" alt="rcc"></kbd>
       - At Connectivity:
       - <kbd><img src="images\i2c1.png" alt="i2c1"></kbd>
       - <kbd><img src="images\usart2.png" alt="usart2"></kbd>
       - <kbd><img src="images\otg.png" alt="otg"></kbd>
       - At Middleware & Software Pack:
       - <kbd><img src="images\middleware.png" alt="middleware"></kbd>
    5. In the end, the pinout view should look like this.
       - <kbd><img src="images\pinout.png" alt="pinout"></kbd>
    6. Finally, generate the code. A main.c file will be generated with all the settings configured. Click the code generation button (Alt + K)
       - <kbd><img src="images\codegenerate.png" alt="codegenerate"></kbd>

---
3. Copy the code in the main.c file
- Simply copy all the code in the main.c file in the repo and paste it all in the main.c file.
---
## Reference

[Getting started with I2C](https://wiki.st.com/stm32mcu/wiki/Getting_started_with_I2C)

[Blackpill pinout](https://stm32world.com/wiki/Black_Pill#Pinout)

[Stm32 Hal I2c and Mpu6050 Imu](https://www.youtube.com/watch?v=P7a6qxacnO4)

[How to Interface MPU6050](https://controllerstech.com/how-to-interface-mpu6050-gy-521-with-stm32/)

[Stm32 Blackpill with USB serial](https://www.bennettnotes.com/notes/stm32-blackpill-with-stmcubeide-usb-serial/)

[Mpu 6050 Arduino Tutorial for Beginners](https://www.youtube.com/watch?v=SVI_NldMjlE)

[Datasheet with I2C Address](https://download.mikroe.com/documents/datasheets/MPU-6000_datasheet.pdf)
