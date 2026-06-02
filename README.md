
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

## 教学视频1： 配置STM32CubeMX的GPIO并且创建Keil工程

## Tutorial Video 1: GPIO Configuration in STM32CubeMX and Keil Project Creation

https://github.com/user-attachments/assets/ac8120e3-7a0f-4d45-a9a8-62b6adbf306c

## 教学视频2：使用 ChatGPT 进行 Keil 编程
## Tutorial Video 2: Keil Programming with ChatGPT
 

## 核心代码

```c
HAL_GPIO_WritePin(GPIOA, GPIO_PIN_0, GPIO_PIN_SET);
HAL_Delay(100);
HAL_GPIO_WritePin(GPIOA, GPIO_PIN_0, GPIO_PIN_RESET);

```

