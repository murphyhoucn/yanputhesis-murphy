# Yet Another NPU Thesis Template - Murphy
> - Forked from [Yet-Another-LaTeX-Template-for-NPU-Thesis](https://github.com/NWPUMetaphysicsOffice/Yet-Another-LaTeX-Template-for-NPU-Thesis)

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![LaTeX](https://img.shields.io/badge/LaTeX-Document-green.svg)](https://www.latex-project.org/)

## 概述

这是一个专为西北工业大学学位论文设计的 LaTeX 模板，支持硕士和博士学位论文的撰写。模板基于 `yanputhesis` 文档类，提供了完整的版本控制功能和模块化结构。

## 环境配置

- 操作系统: Windows 11 Pro 24H2
- TeX 发行版: TeX Live 2024
  - TeX 版本: 3.141592653 (TeX Live 2024)
  - kpathsea 版本: 6.4.0
- 编译器: XeTeX
- 编辑器: VS Code 1.106 + LaTeX Workshop 10.11.3

## 快速开始

### 1. 克隆项目
```bash
git clone git@github.com:murphyhoucn/yanputhesis-murphy.git
cd yanputhesis-murphy
git submodule update --init --recursive
```

### 2. 编辑基本信息

修改 `main.tex` 中的基本信息：

```latex
%% 设置论文类型
% \documentclass[lang=chs, degree=master, blindreview=true, winfonts=true, academic=true]{yanputhesis} % 盲审
\documentclass[lang=chs, degree=master, blindreview=false, winfonts=true, academic=true]{yanputhesis}  % 非盲审
```

### 3. 版本控制说明

本模板采用版本控制结构，可以轻松管理不同版本的论文内容：

```latex
%% 在 main.tex 中设置当前版本
\newcommand{\VersionControl}{Thesis_v1_20250901}
```

目录结构：
```
Thesis_v1_20250901/
├── abstract/
│   ├── chinese-abstract.tex    % 中文摘要
│   └── english-abstract.tex    % 英文摘要
├── acknowledgement/
│   ├── acknowledgements.tex    % 致谢
│   └── accomplishments.tex     % 参加科研情况
├── chapters/
│   ├── chapter01-introduction.tex  % 第一章
│   ├── chapter02-theory.tex        % 第二章
│   ├── chapter03-method_1.tex      % 第三章
│   ├── chapter04-method_2.tex      % 第四章
│   ├── chapter05-conclusion.tex    % 第五章
│   └── appendices.tex              % 附录
└── references/
    └── reference.bib               % 参考文献
```


## 个人记录

## VSCode
`Alt + z`, 切换自动换行与不换行。

## debug command
``` bash
xelatex -interaction=nonstopmode -output-directory=debug main.tex
```

### 《中国图书分类法》- 分类号
- https://www.clcindex.com/category/TP751/
- 中图分类  T 工业技术  TP 自动化技术、计算机技术  TP7 遥感技术  TP75 遥感图像的解译、识别与处理  TP751 图像处理方法

### BibTex
- 直接去论文出版商/期刊网站
- ⭐Google Scholar
- ⭐Semantic Scholar（最佳 Google Scholar 替代）
- DBLP（计算机科学领域神器）：https://dblp.org/search
- https://www.doi2bib.org/

## Jupyterlab

> VSCode 客户端实现不了我想要的在文字编辑时使用触控板双指进行画面缩放！

- 初稿阶段（Overleaf）：在浏览器上进行线上编辑与编译，只考虑内容不考虑排版格式。但在成稿精修期，多平台维护极易导致文档版本不一致。
- 尝试方案（VSCode Remote Tunnels）：虽然能将本地工程映射到浏览器远程修改，但依然不支持触控板双指缩放，阅读体验不佳。
- 最终方案（JupyterLab）：使用 JupyterLab，通过 localhost 启动，既满足了浏览器端顺滑的双指缩放，又能直接对本地文件进行直接编辑与自动保存。无需多平台同步，本地文件即是唯一版本。

## Jupyterlab plugin
- pip install jupyterlab-unfold
- pip install jupyterlab-git
- pip install jupyterlab-latex