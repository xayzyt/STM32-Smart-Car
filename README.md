# STM32 Smart Car

基于 STM32F10x 的智能小车项目，包含程序源码、项目笔记、PCB 资料、BOM 和结构组装资料。

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![STM32](https://img.shields.io/badge/STM32F10x-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white)
![Keil](https://img.shields.io/badge/Keil_MDK-1F6FEB?style=flat-square)

## 功能

- 红外循迹
- 超声波避障
- 超声波跟随
- 蓝牙遥控
- 电机驱动控制
- OLED 显示
- 按键和 LED 调试

## 技术栈

| 项目 | 内容 |
| --- | --- |
| MCU | STM32F10x |
| 语言 | C |
| IDE | Keil MDK |
| 库 | STM32 标准外设库 |
| 外设 | GPIO、EXTI、ADC、Timer、USART、I2C |
| 模块 | 红外、超声波、蓝牙、电机驱动、OLED、按键、LED |

## 目录

| 路径 | 说明 |
| --- | --- |
| `01程序资料/` | Keil 工程和源码 |
| `01程序资料/USER/main.c` | 主程序 |
| `01程序资料/HARDWARE/` | 外设模块代码 |
| `01程序资料/SYSTEM/` | 系统、延时、串口等基础代码 |
| `02笔记资料/` | 项目笔记 |
| `04小车PCB硬件资料.../` | 原理图、PCB、BOM、Gerber |
| `05小车结构组装资料/` | 结构安装资料 |
| `06使用的软件_APP等/` | 串口助手、蓝牙 App 等工具 |

## 使用

1. 安装 Keil MDK 和 STM32F10x 支持包。
2. 打开 `01程序资料/USER/CAR.uvprojx`。
3. 编译工程。
4. 通过 ST-Link 或兼容下载器烧录。
5. 按硬件资料连接红外、超声波、蓝牙、电机驱动和 OLED 模块。

