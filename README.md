# Adaptive Filter Design and Implementation Based on LMS Algorithm

## Overview
This repository contains a signal processing project implemented on the STM32F407 Discovery board. The project focuses on real-time digital signal processing, particularly adaptive filtering using the Least Mean Squares (LMS) algorithm and OFDM communication systems.

## Features
- **LMS Adaptive Filter**: Implementation of the Least Mean Squares algorithm for adaptive filtering
- **Real-time Processing**: Audio processing in real-time with microphone input and speaker output
- **Noise Cancellation**: Effective reduction of unwanted noise in audio signals
- **MATLAB Analysis**: Corresponding MATLAB scripts for algorithm verification and performance analysis

## Hardware Requirements
- STM32F407 Discovery Board
- Audio peripherals (microphone, headphones)
- ST-Link programmer (included on the Discovery board)

## Software Requirements
- PlatformIO (for building and uploading)
- ARM GCC Toolchain
- MATLAB (for running analysis scripts)

## Project Structure
- `src/`: Source code for the STM32 implementation
  - `lab_lms.c/h`: LMS adaptive filter implementation
  - `config.h`: System configuration parameters
  - `main.c`: Main application entry point
- `matlab/`: MATLAB scripts for algorithm testing and visualization
- `matlab_lms/`: MATLAB implementation of LMS algorithm
- `lib/`: External libraries
- `platformio.ini`: PlatformIO configuration file

## Getting Started
1. Clone this repository
2. Open the project in PlatformIO
3. Build and upload to the STM32F407 Discovery board
4. Connect headphones to the audio output jack
5. Run the MATLAB scripts for visualization and analysis

## Results

### System Setup
The following image shows a typical real-world setup for the adaptive filter implementation:

![Real-world Setup](images/Image%20of%20typical%20real-world%20setup.jpg)

The setup includes the STM32F407 Discovery board with audio input/output connections for real-time signal processing.

### Filter Performance

#### Adaptation to Broadband Noise
The following image shows the adaptive filter's performance when cancelling broadband noise:

![Filter Performance with Broadband Noise](images/Filter%20Generated%20in%20Broadband%20Noise.jpg)

The plot demonstrates how the LMS algorithm effectively adapts to reduce broadband noise. The filter coefficients converge to form an appropriate impulse response that minimizes the error between the desired signal and the filtered output.

#### Adaptation to Sinusoidal Noise
The following image shows the adaptive filter's performance when dealing with sinusoidal noise:

![Filter Performance with Sine Noise](images/Filter%20Generated%20in%20Sine%20Noise.jpg)

The plot demonstrates how the LMS algorithm can effectively identify and cancel periodic noise components. The filter adapts specifically to the frequency characteristics of the sinusoidal interference.

## Documentation
- `user_guide.pdf`: Detailed user guide for the development kit
- `Project2_Group3_Rev2.pdf`: Project report with implementation details and results

---

# 基于 LMS 算法的自适应滤波器设计与实现

## 概述
此仓库包含一个在STM32F407 Discovery开发板上实现的信号处理项目。项目专注于实时数字信号处理，特别是使用最小均方（LMS）算法的自适应滤波和OFDM通信系统。

## 特点
- **LMS自适应滤波器**：实现了最小均方算法用于自适应滤波
- **实时处理**：使用麦克风输入和扬声器输出进行实时音频处理
- **噪声消除**：有效减少音频信号中的不需要噪声
- **MATLAB分析**：相应的MATLAB脚本用于算法验证和性能分析

## 硬件要求
- STM32F407 Discovery开发板
- 音频外设（麦克风，耳机）
- ST-Link编程器（Discovery板上已包含）

## 软件要求
- PlatformIO（用于构建和上传）
- ARM GCC工具链
- MATLAB（用于运行分析脚本）

## 项目结构
- `src/`：STM32实现的源代码
  - `lab_lms.c/h`：LMS自适应滤波器实现
  - `config.h`：系统配置参数
  - `main.c`：主应用程序入口点
- `matlab/`：用于算法测试和可视化的MATLAB脚本
- `matlab_lms/`：LMS算法的MATLAB实现
- `lib/`：外部库
- `platformio.ini`：PlatformIO配置文件

## 入门指南
1. 克隆此仓库
2. 在PlatformIO中打开项目
3. 构建并上传到STM32F407 Discovery开发板
4. 将耳机连接到音频输出插孔
5. 运行MATLAB脚本进行可视化和分析

## 实验结果

### 系统设置
下图展示了自适应滤波器实现的典型实际设置：

![实际设置](images/Image%20of%20typical%20real-world%20setup.jpg)

该设置包括STM32F407 Discovery开发板，配有音频输入/输出连接，用于实时信号处理。

### 滤波器性能

#### 宽带噪声适应
下图显示了自适应滤波器在消除宽带噪声时的性能：

![宽带噪声滤波性能](images/Filter%20Generated%20in%20Broadband%20Noise.jpg)

该图表演示了LMS算法如何有效适应并减少宽带噪声。滤波器系数收敛形成适当的脉冲响应，最小化期望信号与滤波输出之间的误差。

#### 正弦噪声适应
下图显示了自适应滤波器处理正弦噪声时的性能：

![正弦噪声滤波性能](images/Filter%20Generated%20in%20Sine%20Noise.jpg)

该图表演示了LMS算法如何有效识别和消除周期性噪声成分。滤波器专门适应正弦干扰的频率特性。

## 文档
- `user_guide.pdf`：开发套件的详细用户指南
- `Project2_Group3_Rev2.pdf`：包含实现细节和结果的项目报告 