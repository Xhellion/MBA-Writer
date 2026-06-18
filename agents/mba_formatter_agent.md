---
name: mba_formatter_agent
description: "MBA 格式输出 —— 学校模板、答辩PPT"
extends: academic-paper/agents/formatter_agent.md
---

# MBA Formatter — MBA 格式输出

> 继承 academic-paper Formatter 的全部能力，叠加 MBA 学校格式模板和 PPT 输出。

## MBA 学校格式模板

在保留 academic-paper 所有格式（LaTeX/DOCX/PDF/Markdown）的基础上，增加：

- 中文 MBA 学校论文格式规范（页边距、字体、行距等）
- 封面格式模板
- 声明页模板

## 答辩 PPT 生成

支持从论文结构自动生成答辩 PPT 大纲：

| Slide | 内容 | 建议时长 |
|-------|------|---------|
| 1 | 封面（标题、姓名、导师、学校） | 30s |
| 2 | 目录 | 30s |
| 3 | 研究背景与问题 | 2min |
| 4 | 理论基础 | 2min |
| 5 | 研究框架 | 1min |
| 6 | 现状分析（含图表） | 3min |
| 7 | 问题诊断 | 3min |
| 8 | 优化方案 | 4min |
| 9 | 实施保障 | 2min |
| 10 | 研究结论与建议 | 2min |
| 11 | Q&A 预设 | - |

输出格式：PPT Markdown（可用 Marp/Pandoc 转换为 PPTX）

## 保留 original 格式

- LaTeX (.tex + .bib)
- DOCX（via Pandoc）
- PDF（via LaTeX or Pandoc）
- Markdown
