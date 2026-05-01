# A Survey of LLM for Computer Architecture / AI4Arch

> A curated literature library for **LLM/Foundation-Model/Agent/RAG methods that assist computer architecture, HLS, simulation, and system co-design**.

> 本仓库整理 **LLM / 基础模型 / Agent / RAG 辅助计算机体系结构、HLS、仿真建模与系统协同优化** 方向的论文、索引表、分类综述和开放 PDF。

## Overview / 项目简介

This project collects papers after the public release of ChatGPT/GPT-3.5 on **2022-11-30**. The inclusion criterion is intentionally narrow: a paper must substantially use an LLM, foundation model, multimodal LLM, agent workflow, or RAG-style system to support architecture or architecture-adjacent design tasks.

本项目从 **2022-11-30** 之后开始收录文献。纳入标准是：论文必须实质使用 LLM、基础模型、多模态大模型、LLM Agent 或 RAG 体系，来辅助计算机体系结构或相关芯片/系统设计任务。

Default exclusions:

- Pure **Arch for AI/LLM** papers, such as accelerators for LLM inference or training, are excluded unless the method uses LLMs to assist architecture design or exploration.
- Traditional ML/RL/BO/GNN-only AI-for-architecture papers are excluded from the main set.
- Pure RTL/Verilog generation papers are kept only as borderline candidates unless they involve architecture exploration, HLS pragmas, PPA tradeoffs, or microarchitectural reasoning.

默认排除：

- 纯粹的 **Arch for AI/LLM**，例如 LLM 推理/训练加速器，除非论文的核心方法是用 LLM 反过来辅助架构设计或探索。
- 传统 ML/RL/BO/GNN-only 的 AI for Architecture 工作不进入主集。
- 纯 RTL/Verilog 生成论文默认放入边界候选，除非涉及架构探索、HLS pragma、PPA tradeoff 或微架构推理。

## Current Snapshot / 当前统计

Search cutoff / 检索截止：**2026-04-30**

| Item | Count |
|---|---:|
| Total records / 总记录 | 34 |
| Main papers / 主集论文 | 27 |
| Borderline candidates / 边界候选 | 7 |
| Downloaded PDFs / 已下载 PDF | 30 |
| Not downloaded / 未下载 | 4 |

## Quick Links / 快速入口

| File | Description |
|---|---|
| [literature_index_by_category.md](AI_for_Arch_LLM_Literature/literature_index_by_category.md) | Compact Markdown index grouped by direction / 按方向分组的快速浏览表 |
| [literature_cards.md](AI_for_Arch_LLM_Literature/literature_cards.md) | Detailed per-paper cards / 逐篇详细卡片 |
| [download_summary.md](AI_for_Arch_LLM_Literature/download_summary.md) | PDF download status and missing reasons / PDF 下载状态和未下载原因 |
| [taxonomy_review.md](AI_for_Arch_LLM_Literature/taxonomy_review.md) | Chinese taxonomy review / 中文分类综述 |
| [literature_index.xlsx](AI_for_Arch_LLM_Literature/literature_index.xlsx) | Spreadsheet index with filters / 可筛选 Excel 表 |
| [literature_index.csv](AI_for_Arch_LLM_Literature/literature_index.csv) | Full CSV index / 完整 CSV 索引 |
| [references.bib](AI_for_Arch_LLM_Literature/references.bib) | BibTeX references / BibTeX 文献库 |
| [download_log.csv](AI_for_Arch_LLM_Literature/download_log.csv) | Download log / 下载日志 |

## Directory Structure / 目录结构

```text
.
├── README.md
├── build_literature_library.py
└── AI_for_Arch_LLM_Literature/
    ├── 01_LLM_Agents_for_DSE/
    ├── 02_LLM_for_Microarchitecture_Policy_Design/
    ├── 03_LLM_for_Simulation_Modeling_and_gem5/
    ├── 04_LLM_for_Performance_Analysis_and_Optimization/
    ├── 05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant/
    ├── 06_LLM_for_HPC_System_Codesign/
    ├── 90_Surveys_Position_and_Vision/
    ├── 99_Candidates_Borderline/
    ├── literature_index_by_category.md
    ├── literature_cards.md
    ├── download_summary.md
    ├── literature_index.xlsx
    ├── literature_index.csv
    ├── references.bib
    └── download_log.csv
```

## Taxonomy / 分类方向

| Directory | Focus |
|---|---|
| [01_LLM_Agents_for_DSE](AI_for_Arch_LLM_Literature/01_LLM_Agents_for_DSE) | LLM/agent-guided design space exploration |
| [02_LLM_for_Microarchitecture_Policy_Design](AI_for_Arch_LLM_Literature/02_LLM_for_Microarchitecture_Policy_Design) | Cache, prefetching, branch prediction, and other microarchitecture policy design |
| [03_LLM_for_Simulation_Modeling_and_gem5](AI_for_Arch_LLM_Literature/03_LLM_for_Simulation_Modeling_and_gem5) | gem5/ChampSim workflows, simulator testing, modeling, and analysis |
| [04_LLM_for_Performance_Analysis_and_Optimization](AI_for_Arch_LLM_Literature/04_LLM_for_Performance_Analysis_and_Optimization) | LLM-assisted performance analysis and compiler/system optimization |
| [05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant](AI_for_Arch_LLM_Literature/05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant) | HLS, RTL, specification, verification, and PPA work when architecture-relevant |
| [06_LLM_for_HPC_System_Codesign](AI_for_Arch_LLM_Literature/06_LLM_for_HPC_System_Codesign) | HPC/GPU/system and software-hardware co-design |
| [90_Surveys_Position_and_Vision](AI_for_Arch_LLM_Literature/90_Surveys_Position_and_Vision) | Surveys, benchmarks, position papers, and vision papers |
| [99_Candidates_Borderline](AI_for_Arch_LLM_Literature/99_Candidates_Borderline) | Borderline EDA/RTL/compiler candidates |

## How to Use / 如何使用

For quick browsing, start with:

```text
AI_for_Arch_LLM_Literature/literature_index_by_category.md
```

For detailed reading, use:

```text
AI_for_Arch_LLM_Literature/literature_cards.md
```

For spreadsheet filtering, open:

```text
AI_for_Arch_LLM_Literature/literature_index.xlsx
```

For citation management, import:

```text
AI_for_Arch_LLM_Literature/references.bib
```

## Reproducibility / 复现方式

The index, Markdown views, BibTeX file, XLSX file, and download log are generated by:

```powershell
python build_literature_library.py
```

The script:

- creates the category directories,
- downloads open PDFs from arXiv/OA/author-public versions when available,
- writes `literature_index.csv` and `literature_index.xlsx`,
- writes Markdown views for quick browsing and detailed reading,
- writes `references.bib`,
- writes `download_log.csv` and `download_summary.md`.

脚本会创建分类目录，优先下载 arXiv/OA/作者公开版 PDF，并同步生成 CSV、XLSX、Markdown、BibTeX 和下载日志。

## PDF and Copyright Notice / PDF 与版权说明

PDF files in this repository are downloaded only from open-access sources such as arXiv, official open versions, or author-public pages. This project does **not** bypass IEEE/ACM or publisher paywalls. When an open PDF was not available or access failed, the official URL, DOI, OA URL, and failure reason are recorded in [download_summary.md](AI_for_Arch_LLM_Literature/download_summary.md) and [download_log.csv](AI_for_Arch_LLM_Literature/download_log.csv).

本仓库中的 PDF 仅来自 arXiv、开放获取版本或作者公开页面。本项目不会绕过 IEEE/ACM 或出版商的闭源访问限制。未能下载的论文会记录正式链接、DOI、开放版本链接和失败原因。

## Status / 维护状态

This is a research literature snapshot as of **2026-04-30**. The field is moving quickly, especially around agentic architecture design, RAG-based trace reasoning, HLS design-space exploration, and LLM-assisted HPC optimization.

这是截至 **2026-04-30** 的研究快照。该方向仍在快速发展，尤其是 agentic architecture design、RAG trace reasoning、HLS DSE 和 LLM-assisted HPC optimization。
