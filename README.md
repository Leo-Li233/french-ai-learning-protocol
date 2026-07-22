# French AI Learning Protocol / 法语AI学习协议

> A student-validated, shareable AI skill package for French learners — built from one semester of real practice.

> 一份经过学生实践验证的、可分享的法语学习AI技能包——基于一学期的真实使用经验。

[![License: CC-BY 4.0](https://img.shields.io/badge/License-CC--BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Status: Case Study](https://img.shields.io/badge/Status-Case%20Study-blue)](https://diidea.pku.edu.cn/)

## 项目背景 | Background

本项目源自第三届全球数智教育创新大赛（AI for Teaching and Learning 赛道）的参赛案例，作者李旭阳（武汉大学法语专业大二学生）通过一学期的实践，建立了一套"战术/战略"双层AI使用模型，并将其编码为可分享的AI技能包。

This project originates from a case study submitted to the 3rd Global Digital Intelligence Education Innovation Competition (AI for Teaching and Learning Track). Through one semester of practice, the author—a sophomore French major at Wuhan University—developed a "tactical/strategic" dual-layer AI usage model and encoded it as a shareable AI skill package.

## 核心理念 | Core Idea

> "在AI时代，最重要的不是会用AI，而是会判断AI什么时候可信、什么时候不可信。"

> "In the AI era, the most important skill is not knowing how to use AI, but knowing when to trust it and when not to."

## 项目结构 | Project Structure

```
french-ai-learning-protocol/
├── README.md                          # 本文件 - 项目概览
├── LICENSE                            # CC-BY 4.0 协议
├── protocol/
│   ├── 01-prompt-templates.md         # 五类提问模板
│   ├── 02-credibility-matrix.md       # AI可信度梯度矩阵
│   ├── 03-error-taxonomy.md           # AI错误分类学
│   └── 04-tool-routing-rules.md       # 工具分层决策规则
├── adapters/
│   ├── README.md                      # 适配器使用说明
│   ├── spanish-adapter.md             # 西班牙语适配器
│   ├── japanese-adapter.md            # 日语适配器
│   └── template-blank.md              # 空白模板（其他语种）
├── evidence/
│   ├── score-comparison.md            # 学业成绩对比
│   ├── reflections/                   # 阶段性反思
│   │   ├── reflection-01-march.md
│   │   ├── reflection-02-april.md
│   │   ├── reflection-03-may.md
│   │   └── reflection-04-june.md
│   └── ai-error-cases.md              # AI错误案例集
├── case-report/
│   ├── competition-submission.md      # 比赛申报表内容
│   └── bilingual-summary.md           # 中英双语摘要
└── website/
    ├── index.html                     # 个人网站首页
    └── style.css                      # 样式表
```

## 快速开始 | Quick Start

### 方法1：使用 Prompt 模板（任何 AI 都适用）

1. 进入 [`protocol/01-prompt-templates.md`](./protocol/01-prompt-templates.md)
2. 根据你当前的学习任务类型（验证/归纳/生成/预测/反思），选择对应模板
3. 复制模板，替换为你的具体内容
4. 粘贴到任何 AI 工具中使用

### 方法2：导入 Claude Project 或 GPT Custom GPT

将整个 `protocol/` 目录的文件上传到 Claude Project 或 GPT Custom GPT 的知识库，然后使用项目指令：

> 你是一名法语学习助手。基于以下规则回答用户：
> 1. 根据问题类型选择回答风格（详见 prompt-templates.md）
> 2. 对自己的回答进行可信度自评（详见 credibility-matrix.md）
> 3. 出现不确定的回答时主动标注可能的风险

### 方法3：跨语种适配（适合其他语言学习者）

1. 进入 [`adapters/`](./adapters/) 目录
2. 找到你的目标语种适配器（如西语、日语）
3. 按照适配器说明调整可信度矩阵的具体值
4. 替换 prompt 模板中的具体法语术语

## 五类提问模板 | Five Prompt Templates

| 类型 | 适用场景 | 模板 |
|---|---|---|
| 验证型 | 写作即时纠错 | "我写的这个句子对吗？错在哪里？" |
| 归纳型 | 零碎知识系统化 | "总结X和Y的核心区别，并各给三个例句" |
| 生成型 | 错题转训练题 | "根据这二十道错题，生成五道同类型训练题" |
| 预测型 | 备考前瞻规划 | "根据考试大纲，预测可能的考点" |
| 反思型 | 错题模式诊断 | "分析我错题的知识盲区并给出补漏计划" |

详细示例见 [`protocol/01-prompt-templates.md`](./protocol/01-prompt-templates.md)。

## AI可信度梯度矩阵 | AI Credibility Matrix

| 任务类型 | 可信度 | 建议验证方式 |
|---|---|---|
| 动词变位验证 | 95%+ | 快速交叉验证 |
| 基础语法纠错 | 90%+ | 对照教材 |
| 固定搭配查询 | 75-85% | 查Larousse或法语助手 |
| 近义词辨析 | 70-80% | 查同义词词典 |
| 文化典故解释 | 50-65% | 查原文资料或请教老师 |
| 文学修辞分析 | 40-55% | 严禁完全依赖AI |

详细说明见 [`protocol/02-credibility-matrix.md`](./protocol/02-credibility-matrix.md)。

## 比赛参赛情况 | Competition Context

- **比赛名称：** 第三届全球数智教育创新大赛
- **赛道：** AI for Teaching and Learning
- **赛组：** 赛组四：AI赋能学习创新案例
- **主办方：** 北京大学、中山大学、复旦大学、西安交通大学等
- **赛程：** 2026年4月28日—8月31日申报
- **颁奖：** 2026年11月北京论坛

## 引用 | Citation

如果本项目对你的研究或学习有帮助，请按以下格式引用：

```bibtex
@misc{li2026french-ai-protocol,
  author = {Li, Xuyang},
  title = {French AI Learning Protocol: A Student-Validated Framework for Strategic AI Use in Language Learning},
  year = {2026},
  publisher = {GitHub},
  url = {https://github.com/[username]/french-ai-learning-protocol}
}
```

## 贡献 | Contributing

欢迎通过 Issue 或 PR 贡献：
- 新的语种适配器（西语已提供，日语待完善）
- 新的 AI 错误类型案例
- 在不同 AI 平台（豆包、ChatGPT、Claude、文心一言等）的使用经验
- 实证研究数据

## 许可 | License

本项目采用 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) 协议授权。你可以自由分享、改编，但需要注明作者和来源。

## 联系方式 | Contact

- **作者：** 李旭阳
- **学校：** 武汉大学外国语学院（法语专业，2024级）
- **邮箱：** 1730610267@qq.com
- **个人网站：** [部署后填入]

---

*本项目是 AI for Teaching and Learning 赛道的参赛作品，旨在通过开源方式让更多学习者受益于经过验证的 AI 使用策略。*
