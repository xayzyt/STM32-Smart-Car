# STM32 Smart Car

基于 **STM32F10x + Keil + STM32 标准外设库** 的智能小车综合实践仓库。这里不仅有程序源码，也整理了原理图、PCB、BOM、装配资料和调试笔记，适合展示一个嵌入式小车项目从硬件资料到软件功能的完整链路。

![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![STM32](https://img.shields.io/badge/STM32F10x-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white)
![Keil](https://img.shields.io/badge/Keil_MDK-1F6FEB?style=flat-square)
![PCB](https://img.shields.io/badge/PCB-JLCEDA-2EA44F?style=flat-square)

## 项目能做什么

- 红外循迹：根据红外对管状态调整运动方向。
- 超声波避障：读取距离信息，完成前方障碍检测和转向策略。
- 超声波跟随：根据目标距离变化调整小车运动。
- 蓝牙遥控：通过串口蓝牙模块接收手机端控制命令。
- 电机控制：完成基础前进、后退、转向、停止等动作。
- OLED / 按键 / LED：用于状态显示、模式切换和调试反馈。

## 为什么这个仓库适合面试展示

很多入门小车只停留在“能跑”。这个仓库更适合讲工程过程：

```text
传感器输入 -> STM32 外设读取 -> 控制逻辑判断 -> 电机驱动输出 -> 小车动作反馈
```

你可以从这里看到我对 STM32 外设、模块化驱动、硬件资料整理和整机调试的基础掌握。

## 技术栈

| 方向 | 内容 |
| --- | --- |
| MCU | STM32F10x |
| Language | C |
| IDE | Keil MDK |
| Driver Library | STM32 标准外设库 |
| Peripherals | GPIO, EXTI, ADC, Timer, USART, I2C |
| Modules | 超声波、红外循迹、蓝牙串口、电机驱动、OLED、按键、LED |
| Hardware | 原理图、PCB 工程、Gerber、BOM、装配图 |

## 仓库结构

| 路径 | 说明 |
| --- | --- |
| `01程序资料/USER/main.c` | 小车主控逻辑入口 |
| `01程序资料/HARDWARE/` | ADC、EXTI、KEY、LED、OLED、TIMER 等外设模块 |
| `01程序资料/SYSTEM/` | 延时、串口、系统配置等基础代码 |
| `01程序资料/STM32F10x_FWLib/` | STM32 标准外设库 |
| `02笔记资料/` | 项目笔记和调试记录 |
| `04小车PCB硬件资料.../` | 原理图、PCB 工程、BOM、Gerber 和 3D/装配资料 |
| `05小车结构组装资料/` | 结构安装图和模块安装说明 |
| `06使用的软件_APP等/` | 串口助手、蓝牙控制 App 等辅助工具 |

## 推荐阅读顺序

1. 先看 `README.md` 理解项目整体。
2. 再看 `01程序资料/USER/main.c`，从主循环和模式切换开始追代码。
3. 进入 `01程序资料/HARDWARE/`，分别看传感器、OLED、按键和定时器模块。
4. 查看 `04小车PCB硬件资料.../`，了解硬件连接和 PCB 资料。
5. 最后看 `02笔记资料/STM32小车笔记V1.0.md`，补充调试过程和细节。

## 如何打开工程

1. 安装 Keil MDK 和 STM32F10x 相关支持包。
2. 打开 `01程序资料/USER/CAR.uvprojx`。
3. 编译工程并通过 ST-Link 或兼容下载器烧录到 STM32F10x 开发板。
4. 按实际接线连接红外、超声波、蓝牙、电机驱动和 OLED 模块。

## 面试时我会重点讲

- 如何把传感器读取、电机控制和模式切换拆成模块。
- 定时器、外部中断、串口在小车项目中的使用方式。
- 红外循迹和超声波避障/跟随的控制逻辑。
- 从原理图、PCB、BOM 到软件调试的完整实践过程。
- 小车类项目如何继续升级：状态机、PID、电机测速、RTOS 任务化。

