# 从森林到农场：可持续农业中的氮动力学建模

<div align="center">
<p>
    <img src="https://img.shields.io/badge/MCM/ICM-2025-blue" alt="竞赛徽章">
    <img src="https://img.shields.io/badge/Award-Finalist-brightgreen" alt="奖项徽章">
    <img src="https://img.shields.io/badge/License-MIT-yellow" alt="许可证徽章">
</p>
</div>
<div align="left">

Click to switch to the English version ☞ **[English](./README.md)** 

</div>

> 🏆 特等奖提名奖 (Finalist Award | 全球27,456支队伍中排名前1.8%)
> -  本仓库包含了我们为 **[2025年MCM/ICM竞赛E题](https://www.contest.comap.com/undergraduate/contests/mcm/contests/2025/problems/2025_ICM_Problem_E.pdf)** 提交的完整解决方案。
> -  我们采用基于改进Lotka-Volterra方程的动态建模方法，模拟了森林与农业生态系统中的氮循环过程，并深入分析了从森林到可持续性农田的生态系统转变。
> -  本项目中包含了论文的**tex源文档**以及**所有代码**。
> -  对于我们论文思路，以及正文讲解，请见 **[本人博客文章](https://www.cnblogs.com/JQ-Luke/p/18858431)**。
> - 推荐阅读顺序：
>   1. 阅读[模型一的jupyter笔记本](./notebooks/1_model_1.ipynb)，包含我对欧拉法与微分方程模型的理解，以及相应的求解代码；
>   2. [中文博客](https://www.cnblogs.com/JQ-Luke/p/18858431)中的思路讲解，最好在读之前先读一遍赛题，明确问题以及我们解决问题的思路；
>   3. 参赛论文和代码（批判性阅读，其实赛后复盘感觉我们有很多点没做好），希望后来者能够吸取我们的经验教训做得更好。

---

## 📖 摘要

将森林转变为农田会极大地改变生态系统的结构与功能。本研究聚焦于作为生态系统健康关键指标的**氮循环**，以探究这些生态后果。我们采用动态建模方法来模拟氮元素在森林和农业食物网中的流动，为人类农业活动带来的影响提供量化分析。

---

## 🔬 核心模型

本研究基于三个递进的核心模型构建：

* **FENCM (森林生态系统氮循环模型):** 一个基础模型，使用改进的Lotka-Volterra方法模拟自然森林食物网中的氮流动，为健康的生态系统建立基准。
* **AENCM (农业生态系统氮循环模型):** FENCM的扩展，该模型纳入了种植、收获、施肥和农药使用等人类干预活动，从而能够模拟不同的耕作策略。
* **AE-FW-NCM (农业生态系统-食物网-氮循环模型):** 最全面的模型，包含一个具有多个营养级的复杂食物网结构，反映了随着时间的推移，一个更加成熟和稳定的农业生态系统。

---

## 📁 仓库结构

为了确保清晰性和可复现性，本仓库按以下结构组织：

```plaintext
MCM-ICM-2025-E-Nitrogen-Cycling-Model/
│
├── .gitignore               # Git忽略配置文件
├── LICENSE                  # MIT许可证文件
├── README.md                # 本文档的英文版
├── README_zh.md             # 本文档（中文版）
├── requirements.txt         # Python项目依赖列表
│
├── notebooks/               # 存放所有的代码与可视化结果
│   ├── 1_model_1.ipynb      # 模型一求解代码，以及我个人对微分方程模型的理解
│   ├── 2_model_2.ipynb      # 模型二 (AENCM) 求解代码
│   ├── 3_model_3.ipynb      # 模型三 (AE-FW-NCM) 求解代码
│   └── 4_sensitivity_anlysis.ipynb # 灵敏度分析求解代码
│
└── paper/                   # 存放完整的学术论文
    ├── main.tex             # LaTeX源文件
    ├── references.bib       # 参考文献
    ├── figures/             # 图片
    └── 2515324.pdf          # 最终的PDF版本论文
```

## 🚀 开始使用
环境要求
- Python 3.8 或更高版本
- Pip 包管理器

### 开始方法一（使用git克隆到本地）
1. 克隆仓库并安装依赖。 以下指令将一次性完成项目配置。
```Bash
git clone https://github.com/LUKEQ420/MCM-ICM-2025-E-Nitrogen-Cycling-Model.git
cd MCM-ICM-2025-E-Nitrogen-Cycling-Model
pip install -r requirements.txt
```

2. 运行分析。 我们完整的工作流程都包含在Jupyter Notebooks中。启动JupyterLab并按顺序运行它们即可复现结果。
```Bash
# 启动 Jupyter Lab 来打开 notebooks
jupyter lab
```
启动JupyterLab后，请进入 `notebooks/` 目录，并从 `1_model_1.ipynb` 开始运行。

### 开始方法二（更推荐采用的简单方式）
1. 点击项目首页（需要切换到上一个页面，即点击切换为中文readme之前的页面）右上方绿色“code”，再点击“download ZIP”直接本地下载安装包并解压
2. 在VS Code中打开解压后的项目文件夹即可本地运行本项目（需要提前在vscode中安装jupyter和latex相关扩展，具体步骤请自行在大模型指导下进行）

*注：由于对本项目感兴趣的可能多为刚接触美赛的本科低年级同学，故更推荐使用这种不使用git的更简单的方式开始*

## ⚖️ 许可证
本项目采用 MIT 许可证发行。更多信息请参见 `LICENSE` 文件。
