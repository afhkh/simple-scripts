---
name: simple-scripts
description: Write or simplify short, directly runnable Python, MATLAB, and similar scripts for learning, coursework, quick experiments, and small local tasks. Use when the user asks for simple code, introductory style, short comments, or one runnable file.
---

# 简单脚本

以初学者能从上往下读懂、能直接运行和能改一个参数再试为目标。用户要短代码时，优先减少要理解的概念和文件数量。

## 写法

- 按题目顺序写。把数据读取、处理和结果展示放在脚本主体，优先用熟悉的循环、判断和标准函数。变量名简短且能看出用途。
- 单个任务通常用一份脚本。重复的计算或题目要求自编的函数可以写成小函数。只有在调用方式或实验要求需要时才增加文件、参数或依赖。
- 中文注释写在步骤前，交代这一步做什么，或某个参数为什么这么取。一段一两句即可。用户给了例子时沿用其命令和组织方式，并核对语法和输出。
- 精简已有代码时，先确定题目要求、输入和需要保留的结果。简化结构后用相同的输入核对关键输出。

## 运行方式

- **Python**：优先提供一个可用 `python 文件名.py` 运行的脚本。小任务优先标准库。随附数据可用 `Path(__file__).resolve().parent` 定位。
- **MATLAB**：优先提供一个能打开并点「运行」的 `.m` 脚本。用 `%%` 按小题分段，需要的局部函数放在末尾。随附图像可用 `fileparts(mfilename('fullpath'))` 找到脚本目录，再用 `fullfile` 拼接路径。
- 有运行环境时，用实际输入从正常入口跑一遍，并检查关键结果。交付时用一句话说明怎么运行、需要什么输入或工具箱。有尚未验证的地方就如实注明。

