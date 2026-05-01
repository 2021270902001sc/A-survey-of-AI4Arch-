# LLM for Computer Architecture 文献分类综述

生成日期：2026-04-30。本库从 2022-11-30 之后开始收录，只纳入实质使用 LLM/基础模型/多模态大模型/Agent/RAG 的工作。当前主集 27 篇，边界候选 7 篇。

## 1. 总体判断

这个方向仍然很新。严格意义上的顶级体系结构 venue 中，已能看到 ASPLOS 2026 的 PF-LLM、CacheMind、LOOPRAG、LPO 等条目，但 ISCA/MICRO/HPCA 近年更多是 Arch for LLM，而不是 LLM for Arch。当前 LLM for Arch 的主阵地集中在 arXiv、HLS/EDA、workshop，以及少量 ASPLOS/期刊论文。

## 2. 技术路线分类

### 01_LLM_Agents_for_DSE: LLM/agent-guided design space exploration
- **gem5 Co-Pilot: AI Assistant Agent for Architectural Design Space Exploration** (2025, CAMS 2025 / arXiv): Natural-language DSE interface; Agentic closed-loop design; RAG/DSDB。目标：gem5 L2 cache hierarchy parameter DSE under cost/power constraints；LLM 角色：LLM state-machine agent analyzes past simulations, proposes gem5 parameter batches, and answers user questions。PDF: `AI_for_Arch_LLM_Literature\01_LLM_Agents_for_DSE\2025_CAMS_2025_Fu_gem5_Co_Pilot_AI_Assistant_Agent_for_Architectur.pdf`
- **LLM-DSE: Searching Accelerator Parameters with LLM Agents** (2025, arXiv): Agentic closed-loop design。目标：HLS directive/parameter optimization for domain-specific accelerators；LLM 角色：Router, Specialist, Arbitrator, and Critic agents guide parameter search with online verbal learning。PDF: `AI_for_Arch_LLM_Literature\01_LLM_Agents_for_DSE\2025_arXiv_Wang_LLM_DSE_Searching_Accelerator_Parameters_with_LL.pdf`
- **iDSE: Navigating Design Space Exploration in High-Level Synthesis Using LLMs** (2025, arXiv): Natural-language/DSE reasoning; Agentic closed-loop design。目标：HLS directive configurations and generated microarchitectures；LLM 角色：LLM prunes design space, generates warm-start samples, reflects on QoR trajectories, and refines Pareto designs。PDF: `AI_for_Arch_LLM_Literature\01_LLM_Agents_for_DSE\2025_arXiv_Li_iDSE_Navigating_Design_Space_Exploration_in_High.pdf`
- **MPM-LLM4DSE: Reaching the Pareto Frontier in HLS with Multimodal Learning and LLM-Driven Exploration** (2026, arXiv): LLM optimizer with multimodal QoR predictor。目标：HLS pragma configuration / accelerator design；LLM 角色：LLM acts as optimizer guided by pragma-impact prompt engineering; code text embeddings augment prediction。PDF: `AI_for_Arch_LLM_Literature\01_LLM_Agents_for_DSE\2026_arXiv_Xu_MPM_LLM4DSE_Reaching_the_Pareto_Frontier_in_HLS.pdf`

### 02_LLM_for_Microarchitecture_Policy_Design: Microarchitecture policy design and reasoning
- **PF-LLM: Large Language Model Hinted Hardware Prefetching** (2026, ASPLOS 2026): LLM-assisted microarchitecture policy design。目标：hardware prefetching / processor microarchitecture；LLM 角色：LLM hints hardware prefetching policy/design choices。PDF: `AI_for_Arch_LLM_Literature\02_LLM_for_Microarchitecture_Policy_Design\2026_ASPLOS_2026_Xu_PF_LLM_Large_Language_Model_Hinted_Hardware_Pref.pdf`
- **CacheMind: From Miss Rates to Why -- Natural-Language, Trace-Grounded Reasoning for Cache Replacement** (2026, ASPLOS 2026 / arXiv): RAG/trace-grounded reasoning。目标：cache replacement；LLM 角色：Conversational RAG system explains cache traces and replacement behavior。PDF: `AI_for_Arch_LLM_Literature\02_LLM_for_Microarchitecture_Policy_Design\2026_ASPLOS_2026_Mhapsekar_CacheMind_From_Miss_Rates_to_Why_Natural_Languag.pdf`
- **Agentic Architect: An Agentic AI Framework for Architecture Design Exploration and Optimization** (2026, arXiv): Agentic closed-loop design。目标：cache replacement; data prefetching; branch prediction；LLM 角色：LLM agent evolves code/design policies under simulator feedback。PDF: `AI_for_Arch_LLM_Literature\02_LLM_for_Microarchitecture_Policy_Design\2026_arXiv_Blasberg_Agentic_Architect_An_Agentic_AI_Framework_for_Ar.pdf`

### 03_LLM_for_Simulation_Modeling_and_gem5: Architecture simulation, modeling, gem5/ChampSim workflows
- **SearchGEM5: Towards Reliable gem5 with Search Based Software Testing and Large Language Models** (2023, SSBSE 2023 / LNCS): LLM for simulation workflow。目标：gem5 system simulator reliability；LLM 角色：ChatGPT parameterizes C programs that seed a custom AFL++ fuzzing flow。PDF: `AI_for_Arch_LLM_Literature\03_LLM_for_Simulation_Modeling_and_gem5\2023_SSBSE_2023_Dakhama_SearchGEM5_Towards_Reliable_gem5_with_Search_Bas.pdf`
- **Enhancing Search-Based Testing with LLMs for Finding Bugs in System Simulators** (2025, Automated Software Engineering): LLM for simulation workflow。目标：gem5 system simulator reliability；LLM 角色：Six LLMs generate structured test inputs that seed customized AFL++ mutation and differential testing。PDF: `AI_for_Arch_LLM_Literature\03_LLM_for_Simulation_Modeling_and_gem5\2025_Automated_Software_E_Dakhama_Enhancing_Search_Based_Testing_with_LLMs_for_Fin.pdf`

### 04_LLM_for_Performance_Analysis_and_Optimization: Performance analysis and optimization
- **LOOPRAG: Enhancing Loop Transformation Optimization with Retrieval-Augmented Large Language Models** (2026, ASPLOS 2026): Cross-layer/HPC optimization。目标：loop transformation and performance portability; architecture-adjacent compiler optimization；LLM 角色：RAG augments LLM loop-transformation optimizer。PDF: `AI_for_Arch_LLM_Literature\04_LLM_for_Performance_Analysis_and_Optimization\2026_ASPLOS_2026_Zhi_LOOPRAG_Enhancing_Loop_Transformation_Optimizati.pdf`
- **LPO: Discovering Missed Peephole Optimizations with Large Language Models** (2026, ASPLOS 2026): Cross-layer/HPC optimization。目标：compiler optimization; systems/compiler layer adjacent to architecture；LLM 角色：LLM discovers missed peephole optimizations。PDF: `AI_for_Arch_LLM_Literature\04_LLM_for_Performance_Analysis_and_Optimization\2026_ASPLOS_2026_Xu_LPO_Discovering_Missed_Peephole_Optimizations_wi.pdf`

### 05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant: HLS/RTL/specification/verification when architecture-relevant
- **LIFT: LLM-Based Pragma Insertion for HLS via GNN Supervised Fine-Tuning** (2025, arXiv): Hardware design/spec optimization with LLM fine-tuning。目标：FPGA/HLS microarchitecture transformations；LLM 角色：Fine-tuned LLM generates performance-critical pragmas with GNN supervision。PDF: `AI_for_Arch_LLM_Literature\05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant\2025_arXiv_Prakriya_LIFT_LLM_Based_Pragma_Insertion_for_HLS_via_GNN.pdf`
- **DiffHLS: Differential Learning for High-Level Synthesis QoR Prediction with GNNs and LLM Code Embeddings** (2026, arXiv): Surrogate/QoR prediction augmented by pretrained code LLM embeddings。目标：HLS pragma-driven design variants；LLM 角色：Pretrained code LLM embeddings improve delta-path QoR prediction。PDF: `AI_for_Arch_LLM_Literature\05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant\2026_arXiv_Peng_DiffHLS_Differential_Learning_for_High_Level_Syn.pdf`
- **ChatHLS: Towards Systematic Design Automation and Optimization for High-Level Synthesis** (2025, arXiv): LLM for simulation workflow; hardware design/spec optimization。目标：HLS code and accelerator design；LLM 角色：Fine-tuned LLMs in multi-agent framework for HLS-C debugging and QoR-aware directive optimization。PDF: `AI_for_Arch_LLM_Literature\05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant\2025_arXiv_Li_ChatHLS_Towards_Systematic_Design_Automation_and.pdf`
- **HLStrans: Dataset for C-to-HLS Hardware Code Synthesis** (2025, OpenReview / arXiv, submitted to ICLR 2026): Benchmark/dataset; hardware design/spec optimization。目标：FPGA/HLS program transformations and pragmas；LLM 角色：LLMs are benchmarked and used in augmentation pipeline with MCTS/DSE。PDF: `AI_for_Arch_LLM_Literature\05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant\2025_OpenReview_Zou_HLStrans_Dataset_for_C_to_HLS_Hardware_Code_Synt.pdf`
- **HLSPilot: LLM-based High-Level Synthesis** (2024, ICCAD 2024 / arXiv): LLM for simulation workflow; hardware/software co-design; DSE tool use。目标：hybrid CPU-FPGA accelerators and HLS-generated microarchitectures；LLM 角色：LLM profiles software, identifies bottlenecks, retrieves HLS strategies, generates optimized HLS code, invokes DSE tooling, and helps CPU-FPGA deployment。PDF: `AI_for_Arch_LLM_Literature\05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant\2024_ICCAD_2024_Xiong_HLSPilot_LLM_based_High_Level_Synthesis.pdf`
- **HLS-Eval: A Benchmark and Framework for Evaluating LLMs on High-Level Synthesis Design Tasks** (2025, IEEE ICLAD 2025 / arXiv): Benchmark/dataset; hardware design/spec optimization。目标：HLS designs for accelerators and hardware systems；LLM 角色：Evaluates LLMs for HLS code generation and HLS-specific code edits targeting performance/hardware efficiency。PDF: `AI_for_Arch_LLM_Literature\05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant\2025_IEEE_ICLAD_2025_Abi_Karam_HLS_Eval_A_Benchmark_and_Framework_for_Evaluatin.pdf`
- **SAGE-HLS: Syntax-Aware AST-Guided LLM for High-Level Synthesis Code Generation** (2025, arXiv): Hardware design/spec optimization。目标：HLS code for FPGA/ASIC hardware generation；LLM 角色：Fine-tuned LLM uses AST-guided instruction prompting and Verilog-to-C/C++ porting to improve synthesizable HLS code generation。PDF: `AI_for_Arch_LLM_Literature\05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant\2025_arXiv_Khan_SAGE_HLS_Syntax_Aware_AST_Guided_LLM_for_High_Le.pdf`
- **Bench4HLS: End-to-End Evaluation of LLMs in High-Level Synthesis Code Generation** (2026, arXiv): Benchmark/dataset; hardware design/spec optimization。目标：HLS designs from small kernels to complex accelerators；LLM 角色：Benchmarks LLM-generated HLS designs through compilation, simulation, synthesis, and PPA analysis。PDF: `AI_for_Arch_LLM_Literature\05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant\2026_arXiv_Khan_Bench4HLS_End_to_End_Evaluation_of_LLMs_in_High.pdf`
- **High-level Synthesis Directives Design Optimization via Large Language Model** (2025, ACM Transactions on Design Automation of Electronic Systems): Hardware design/spec optimization; Agentic closed-loop design。目标：HLS directives and FPGA design space exploration；LLM 角色：Uses LLMs as feature extractors and autonomous agents for HLS directive optimization。PDF: 未下载或未找到开放版本
- **TimelyHLS: LLM-Based Timing-Aware and Architecture-Specific FPGA HLS Optimization** (2025, IEEE COINS 2025 / arXiv): RAG/trace-grounded reasoning; hardware design/spec optimization。目标：FPGA-specific HLS code and RTL quality；LLM 角色：LLM with RAG generates and iteratively refines timing- and architecture-specific pragmas from synthesis feedback。PDF: `AI_for_Arch_LLM_Literature\05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant\2025_IEEE_COINS_2025_Mashnoor_TimelyHLS_LLM_Based_Timing_Aware_and_Architectur.pdf`

### 06_LLM_for_HPC_System_Codesign: HPC/system/software-hardware co-design
- **Optimas: An Intelligent Analytics-Informed Generative AI Framework for Performance Optimization** (2026, arXiv): Cross-layer/HPC optimization。目标：NVIDIA GPU code/performance optimization；LLM 角色：Multi-agent workflow maps performance diagnostics to literature-backed code transformations and validates execution。PDF: `AI_for_Arch_LLM_Literature\06_LLM_for_HPC_System_Codesign\2026_arXiv_Zaeed_Optimas_An_Intelligent_Analytics_Informed_Genera.pdf`
- **SwizzlePerf: Hardware-aware LLMs for GPU Kernel Performance Optimization** (2025, arXiv): Cross-layer/HPC optimization。目标：GPU kernels and hardware-aware code transformation；LLM 角色：LLM assists hardware-aware kernel performance optimization。PDF: `AI_for_Arch_LLM_Literature\06_LLM_for_HPC_System_Codesign\2025_arXiv_Tschand_SwizzlePerf_Hardware_aware_LLMs_for_GPU_Kernel_P.pdf`

### 90_Surveys_Position_and_Vision: Surveys, benchmarks, position papers, vision papers
- **QuArch: A Benchmark for Evaluating LLM Reasoning in Computer Architecture** (2025, OpenReview / arXiv, submitted to ICLR 2026): Benchmark/dataset for architecture reasoning。目标：processor design; memory systems; interconnection networks；LLM 角色：Evaluates LLM architecture knowledge, analysis, design, and implementation reasoning。PDF: `AI_for_Arch_LLM_Literature\90_Surveys_Position_and_Vision\2025_OpenReview_Prakash_QuArch_A_Benchmark_for_Evaluating_LLM_Reasoning.pdf`
- **Large Processor Chip Model** (2025, arXiv / Science China Information Sciences for review): Survey/vision; Agentic closed-loop design。目标：processor/chip architecture across software-hardware stack；LLM 角色：LPCM proposes LLM/agent levels for compiler, binary translation, simulator, partitioning, DSE, RTL generation。PDF: `AI_for_Arch_LLM_Literature\90_Surveys_Position_and_Vision\2025_arXiv_Chang_Large_Processor_Chip_Model.pdf`
- **Hardware Design and Verification with Large Language Models: A Scoping Review, Challenges, and Open Issues** (2025, Electronics): Survey/vision。目标：chip architecture; RTL; verification; physical design；LLM 角色：Reviews LLM use across specification, RTL, verification, chip architecture design, and EDA workflows。PDF: 未下载或未找到开放版本
- **Report for NSF Workshop on AI for Electronic Design Automation** (2024, NSF Workshop Report): Survey/vision。目标：EDA and hardware design flows；LLM 角色：Discusses LLMs, GNNs, RL and AI methods for HLS/LLS, optimization, physical synthesis, test and verification。PDF: 未下载或未找到开放版本

## 3. 代表性趋势

- **从聊天助手到闭环代理**：gem5 Co-Pilot、LLM-DSE、iDSE、Agentic Architect 都把 LLM 放进“生成候选设计-调用工具-读取反馈-再生成”的闭环。
- **从性能数字到可解释原因**：CacheMind 这类 RAG/trace-grounded 方法开始让 LLM 面向 cache trace、PC、地址和策略行为做可验证解释。
- **HLS 是最活跃落点**：因为 HLS 的 pragma/DSE 空间巨大且评估昂贵，LLM 的知识推理、代码理解和探索策略比较容易形成闭环。
- **严格微架构策略设计刚起步**：PF-LLM、Agentic Architect、CacheMind 是最贴近 cache/prefetch/branch predictor 的方向，数量还少但增长快。
- **评测基础正在出现**：QuArch 开始系统测 LLM 的体系结构知识、分析、设计和实现能力。

## 4. 最近半年 arXiv 重点

- 2026-02-12：**CacheMind: From Miss Rates to Why -- Natural-Language, Trace-Grounded Reasoning for Cache Replacement**，LLM for cache replacement reasoning。
- 2026-04-28：**Agentic Architect: An Agentic AI Framework for Architecture Design Exploration and Optimization**，agentic microarchitecture design。
- 2026-01-08：**MPM-LLM4DSE: Reaching the Pareto Frontier in HLS with Multimodal Learning and LLM-Driven Exploration**，LLM-driven HLS Pareto DSE。
- 2026-04-10：**DiffHLS: Differential Learning for High-Level Synthesis QoR Prediction with GNNs and LLM Code Embeddings**，LLM code embeddings for HLS QoR prediction。
- 2026-01-16：**Bench4HLS: End-to-End Evaluation of LLMs in High-Level Synthesis Code Generation**，end-to-end benchmark for LLM-generated HLS。
- 2026-03-24：**LOOPRAG: Enhancing Loop Transformation Optimization with Retrieval-Augmented Large Language Models**，compiler optimization with RAG LLMs。
- 2026-04：**Optimas: An Intelligent Analytics-Informed Generative AI Framework for Performance Optimization**，LLM agents for GPU/HPC performance optimization。

## 5. 边界候选说明

以下论文是 EDA/RTL/Verilog/规范生成方向，未必属于 computer architecture 主集，但对构建 LLM-for-chip/architecture 工具链很有参考价值：

- **ChipNeMo: Domain-Adapted LLMs for Chip Design** (2023): Important chip-design LLM paper, but broader EDA rather than computer architecture.
- **Verigen: A Large Language Model for Verilog Code Generation** (2024): Pure RTL-generation baseline; included as borderline due EDA extension.
- **RTLLM: An Open-Source Benchmark for Design RTL Generation with Large Language Model** (2024): Strong EDA benchmark; not architecture-specific but useful as foundation.
- **RTLCoder: Outperforming GPT-3.5 in Design RTL Generation with Our Open-Source Dataset and Lightweight Solution** (2023): Pure RTL-generation; included as candidate.
- **SpecLLM: Exploring Generation and Review of VLSI Design Specification with Large Language Model** (2024): Specification-level rather than architecture evaluation; include as borderline.
- **From English to ASIC: Hardware Implementation with Large Language Model** (2024): Natural-language hardware implementation; kept as EDA candidate.
- **Advanced Language Model-Driven Verilog Development: Enhancing Power, Performance, and Area Optimization in Code Synthesis** (2023): PPA angle makes it somewhat architecture-relevant, but still mostly RTL/EDA.

## 6. 明确排除原则

- 只讨论如何加速/部署 LLM 的硬件架构论文，如果没有用 LLM 来辅助设计或优化，默认排除。
- 传统 ML/RL/BO/GNN-only 的 AI for Architecture 工作不进入本库主集。
- 纯 RTL 代码生成论文放在边界候选，除非显式涉及架构级 DSE、PPA tradeoff、HLS pragma 或微架构策略。