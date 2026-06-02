
## STM32 HAL LED Flow Light Experiment Based on STM32F103C8T6 with ChatGPT  
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
* 杜邦线
* USB 下载器：例如 ST-Link（需要安装驱动），推荐使用 DAP-Link（免驱）

## 需要的软件工具 
* Keil
* STM32CubeMX 
## Software Requirements

- Keil
- STM32CubeMX
## Required Hardware

* STM32F103 development board
* LED module or onboard LEDs
* Dupont wires
* USB programmer/debugger: for example, ST-Link requires driver installation, while DAP-Link is usually driver-free

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

## 效果图

## Demo Image
## 教学视频0： 安装STM32CubeM，安装 Keil 
## Tutorial Video 0: Installing STM32CubeMX and Keil
请谷歌搜索安装教程，或者询问ChatGPT

Please search for installation tutorials on Google, or ask ChatGPT for guidance.

教学视频0要实现的目标：能打开STM32CubeM和Keil 

Tutorial Video 0 Goal:After completing this tutorial, you should be able to open STM32CubeMX and Keil successfully.
## 教学视频1： 配置STM32CubeMX的GPIO并且创建Keil工程
教学视频1要实现的目标：

- 1.配置GPIO
- 2.配置RCC
- 3.配置SYS
- 4.配置配置时钟树
- 5.配置工程名字并和存储文件夹的位置
- 6.其他相关设置
- 7.生成Keil工程并且编译通过

## Tutorial Video 1: GPIO Configuration in STM32CubeMX and Keil Project Creation



https://github.com/user-attachments/assets/25778a27-5b26-4297-9fab-60124dad6223



## 教学视频2：使用 ChatGPT 进行 Keil 编程
## Tutorial Video 2: Keil Programming with ChatGPT
 

https://github.com/user-attachments/assets/3921d96a-85ed-4ba0-9f5e-435d06ce9df7



## 核心代码

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

