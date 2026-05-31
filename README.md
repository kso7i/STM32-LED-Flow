# STM32 LED Flow Light

STM32 HAL LED flow light example for beginners


这是一个基于 STM32 HAL 库的流水灯入门项目，适合刚开始学习 STM32 GPIO 输出控制的同学。

## 项目功能

使用 STM32 控制多个 LED 依次点亮，实现基础流水灯效果。

## 使用硬件

- STM32F103 开发板
- LED 模块或板载 LED
- 杜邦线
- USB 下载器 / ST-Link

## 引脚连接

| LED | STM32 引脚 |
|---|---|
| LED1 | PA0 |
| LED2 | PA1 |
| LED3 | PA2 |
| LED4 | PA3 |
| LED5 | PA4 |
| LED6 | PA5 |
| LED7 | PA6 |
| LED8 | PA7 |

## 效果图

<img width="1827" height="1827" alt="kiki_4_happy-1961966506428043505-img1" src="https://github.com/user-attachments/assets/ba38f880-43e3-4892-8183-2d05831d037b" />

## 核心代码

```c
HAL_GPIO_WritePin(GPIOA, GPIO_PIN_0, GPIO_PIN_SET);
HAL_Delay(100);
HAL_GPIO_WritePin(GPIOA, GPIO_PIN_0, GPIO_PIN_RESET);

```
学习重点
GPIO 输出模式
HAL_GPIO_WritePin 函数
HAL_Delay 延时函数
STM32CubeMX 配置 GPIO
