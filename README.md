# 多专家情感数字人系统

## 项目简介

本系统是一个集成了多模态情感分析、数字人驱动和共情对话的智能交互系统。支持文本、声音、视觉三种模态的情感分析，通过多专家融合机制准确识别用户情绪，并驱动数字人做出相应的表情和语音反馈。



## 模型下载说明

注意：模型文件需要单独下载，本仓库只包含代码。

本项目依赖以下预训练模型，因体积较大未包含在仓库中：

### 1. Qwen2.5-7B-Instruct（对话生成）
- **下载地址**：[ModelScope](https://modelscope.cn/models/Qwen/Qwen2.5-7B-Instruct) 或 [HuggingFace](https://huggingface.co/Qwen/Qwen2.5-7B-Instruct)
- **放置路径**：’在项目根下创建/model_llm/Qwen2.5-7B-Instruct/`

### 2. 情感分析模型SenseVioceSmall（语音）
- **下载地址**：https://www.modelscope.cn/models/iic/SenseVoiceSmall
- **放置路径**： `在项目根下创建/emotion_model_sound/`

## 快速开始

1. 安装依赖：`pip install -r requirements.txt`
2. 运行：`python actdigital_human_system.py`

### 核心功能

- **多模态情感分析**：融合文本、语音、视觉三种模态，准确识别用户情绪
- **高风险检测**：实时检测自杀倾向、严重负面情绪等高风险信号
- **数字人驱动**：通过UDP协议控制数字人表情和语音
- **共情对话**：集成Qwen2.5大语言模型，生成富有共情力的回复
- **会话管理**：支持多用户会话，记录情感变化趋势

---

## 系统要求

### 硬件要求

| 配置项 | 最低要求 | 推荐配置 |
|--------|----------|----------|
| CPU | Intel i5 / AMD Ryzen 5 | Intel i7 / AMD Ryzen 7 |
| 内存 | 8GB | 16GB+ |
| 显卡 | 无（CPU模式） | NVIDIA RTX 3060+ (8GB+) |
| 硬盘 | 20GB可用空间 | 50GB+ SSD |

### 软件要求

- Windows 10/11 或 Linux (Ubuntu 20.04+)
- Python 3.8 - 3.10
- CUDA 11.7+ (如需GPU加速)

---

## 快速开始

### 1. 安装Python依赖

```bash
pip install -r requirements.txt

窗口1: Unity数字人程序（本仓库没有数字人程序，需连接你的exe程序）
       └── 双击 zzzzzzzzzzzz.exe

窗口2: API服务器
       └── python api_server.py

 