
## STM32 LED Flow Light Experiment Based on STM32F103C8T6 Using ChatGPT and the HAL Library
STM32 HAL 库的流水灯实验（基于STMF103C8T6）


本项目以 STM32F103C8T6 芯片为例，也可以使用其他 STM32 芯片，基本 GPIO 控制原理都是通用的。

This project uses the STM32F103C8T6 as an example. Other STM32 chips can also be used, because the basic GPIO control principle is generally the same.

## 中文说明

这是一个基于 STM32 HAL 库的流水灯入门项目，适合刚开始学习 STM32 GPIO 输出控制的同学。

本项目使用 ChatGPT 辅助生成相关代码和文档说明，帮助初学者更快理解 STM32 GPIO 输出控制的基本流程。

## English Description

This is a beginner-friendly LED flow light project based on the STM32 HAL library. It is suitable for students who are just starting to learn STM32 GPIO output control.

ChatGPT was used to assist with code generation and documentation, helping beginners understand the basic workflow of STM32 GPIO output control more efficiently.
 
## 项目功能：使用 STM32 控制多个 LED 依次点亮，实现基础流水灯效果。
Use an STM32 microcontroller to control multiple LEDs and turn them on one by one, creating a basic LED flow light effect. 

## 学习重点

- STM32CubeMX 配置 GPIO
- GPIO 输出模式
- 使用 Keil 软件编程
- `HAL_GPIO_WritePin()` 函数
- `HAL_Delay()` 延时函数

## Learning Points

- STM32CubeMX GPIO configuration
- GPIO output mode
- Programming with Keil
- `HAL_GPIO_WritePin()` function
- `HAL_Delay()` delay function

## 需要的硬件实物

* STM32F103 开发板
* LED 模块或板载 LED
* 杜邦线和面包板
* USB 下载器：例如 ST-Link（需要安装驱动），推荐使用 DAP-Link（免驱）
* 1KΩ 电阻

## Required Hardware Components
* STM32F103 development board
* LED module or onboard LED
* Jumper wires and a breadboard
* USB programmer/debugger: for example, ST-Link, which requires driver installation. DAP-Link is recommended because it is driver-free.
* 1 kΩ resistor



## 需要的软件工具 
* Keil
* STM32CubeMX 
* 请根据需要下载并安装仓库的相关驱动

## Required Software Tools
* Keil
* STM32CubeMX
* Please download the CH340 driver and ST-LINK driver from the Releases section of this repository if needed.



## 引脚连接

| LED  | STM32 引脚 |
| ---- | -------- |
| LED1 | PA0      |
| LED2 | PA1      |
| LED3 | PA2      |
| LED4 | PA3      |

## Pin Connection

| LED  | STM32 Pin |
| ---- | --------- |
| LED1 | PA0       |
| LED2 | PA1       |
| LED3 | PA2       |
| LED4 | PA3       |
## 原理图和实物接线图
## Schematic Diagram and Physical Wiring Diagram
<img width="1247" height="731" alt="Schematic Diagram" src="https://github.com/user-attachments/assets/866d4bf4-c1a3-4d42-8154-c02207ae0d62" />
<img width="4000" height="3000" alt="Physical Wiring Diagram" src="https://github.com/user-attachments/assets/a787f076-6a08-4b79-a443-89ca191ed9b0" />


## 教学视频0： 安装STM32CubeMX，安装 Keil 
## Tutorial Video 0: Installing STM32CubeMX and Keil
请谷歌搜索安装教程，或者询问ChatGPT

Please search for installation tutorials on Google, or ask ChatGPT for guidance.

教学视频0要实现的目标：能打开STM32CubeM和Keil 

Tutorial Video 0 Goal:After completing this tutorial, you should be able to open STM32CubeMX and Keil successfully.
## 教学视频1： 配置STM32CubeMX的GPIO并且创建Keil工程
## Tutorial Video 1: GPIO Configuration in STM32CubeMX and Keil Project Creation
教学视频1要实现的目标：

- 1.配置GPIO的PA0,PA1,PA2,PA3 
- 2.配置RCC
- 3.配置SYS
- 4.配置配置时钟树
- 5.配置工程名字并和存储文件夹的位置
- 6.其他相关设置
- 7.生成Keil工程并且编译通过

## Tutorial Video 1: Objectives

- Configure GPIO PA0,PA1,PA2,PA3 
- Configure RCC
- Configure SYS
- Configure the clock tree
- Set the project name and project save location
- Complete other related settings
- Generate the Keil project and make sure it compiles successfully



https://github.com/user-attachments/assets/25778a27-5b26-4297-9fab-60124dad6223



## 教学视频2：使用 ChatGPT 进行 Keil 编程
## Tutorial Video 2: Keil Programming with ChatGPT
教学视频2要实现的目标：输入核心代码到main()函数的 while (1){}循环里

Tutorial Video 2: Objective: Enter the core code into the `while (1) {}` loop inside the `main()` function.**
## 核心代码
## Core Code
```c
    HAL_GPIO_WritePin(GPIOA, GPIO_PIN_1, GPIO_PIN_SET);
    HAL_Delay(200);
    HAL_GPIO_WritePin(GPIOA, GPIO_PIN_1, GPIO_PIN_RESET);

    HAL_GPIO_WritePin(GPIOA, GPIO_PIN_2, GPIO_PIN_SET);
    HAL_Delay(200);
    HAL_GPIO_WritePin(GPIOA, GPIO_PIN_2, GPIO_PIN_RESET);

    HAL_GPIO_WritePin(GPIOA, GPIO_PIN_3, GPIO_PIN_SET);
    HAL_Delay(200);
    HAL_GPIO_WritePin(GPIOA, GPIO_PIN_3, GPIO_PIN_RESET);

    HAL_GPIO_WritePin(GPIOA, GPIO_PIN_4, GPIO_PIN_SET);
    HAL_Delay(200);
    HAL_GPIO_WritePin(GPIOA, GPIO_PIN_4, GPIO_PIN_RESET);

```




 

https://github.com/user-attachments/assets/3921d96a-85ed-4ba0-9f5e-435d06ce9df7

## 教学视频3：使用Keil下载hex文件
## Tutorial Video 3: Downloading the HEX File with Keil 
教学视频3要实现的目标：成功下载

Objective of Tutorial Video 3: Download the program successfully.


https://github.com/user-attachments/assets/99a7db45-5897-492d-9604-65ae8dd509a1
## 手动复位芯片。得到最终的效果
## Manually reset the chip to see the final result.

https://github.com/user-attachments/assets/2950ba71-0bfd-4824-aaa8-51fa5051d00b

## 教学视频4：下载我的已经编译好的仓库工程文件并且下载到芯片
## Tutorial Video 4: Downloading the Precompiled Project Files from My Repository and Programming Them to the Chip


https://github.com/user-attachments/assets/05366f73-20ba-445d-b8f4-75abe4faa2e7


