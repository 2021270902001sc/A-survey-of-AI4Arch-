# Literature Cards

Detailed per-paper Markdown view. Use `literature_index_by_category.md` for quick scanning.

## 01_LLM_Agents_for_DSE

LLM/agent-guided design space exploration.

### 1. MPM-LLM4DSE: Reaching the Pareto Frontier in HLS with Multimodal Learning and LLM-Driven Exploration

- **ID:** `mpm_llm4dse_2026`
- **Authors:** Lei Xu; Shanshan Wang; Chenglong Xiao
- **Year / Venue:** 2026 / arXiv
- **Paper type:** recent preprint
- **Status:** main; recent arXiv
- **Direction:** LLM-driven HLS Pareto DSE
- **Technical route:** LLM optimizer with multimodal QoR predictor
- **LLM role:** LLM acts as optimizer guided by pragma-impact prompt engineering; code text embeddings augment prediction
- **Architecture target:** HLS pragma configuration / accelerator design
- **Simulator/toolchain:** HLS synthesis data; multimodal prediction model; ProgSG baseline
- **Evaluation metrics:** up to 10.25x QoR-prediction improvement; 39.90% DSE performance gain over prior methods
- **PDF:** [PDF](<01_LLM_Agents_for_DSE/2026_arXiv_Xu_MPM_LLM4DSE_Reaching_the_Pareto_Frontier_in_HLS.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2601.04801>)
- **DOI/arXiv:** arXiv:2601.04801
- **Notes:** Recent half-year arXiv; HLS-specific but strongly DSE-oriented.

### 2. gem5 Co-Pilot: AI Assistant Agent for Architectural Design Space Exploration

- **ID:** `gem5_copilot_2025`
- **Authors:** Zuoming Fu; Alexander M. Manley; Mohammad Alian
- **Year / Venue:** 2025 / CAMS 2025 / arXiv
- **Paper type:** workshop paper / preprint
- **Status:** main
- **Direction:** LLM agent for gem5 DSE
- **Technical route:** Natural-language DSE interface; Agentic closed-loop design; RAG/DSDB
- **LLM role:** LLM state-machine agent analyzes past simulations, proposes gem5 parameter batches, and answers user questions
- **Architecture target:** gem5 L2 cache hierarchy parameter DSE under cost/power constraints
- **Simulator/toolchain:** gem5; McPAT; Design Space Declarative Language; Design Space Database; Streamlit UI
- **Evaluation metrics:** near-optimal perf_ratio with 2-12 gem5 runs; API cost below 0.5 USD/session
- **PDF:** [PDF](<01_LLM_Agents_for_DSE/2025_CAMS_2025_Fu_gem5_Co_Pilot_AI_Assistant_Agent_for_Architectur.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2510.19577>) / [OA](<https://wisl.ece.cornell.edu/papers/gem5-co-pilot-cams-25.pdf>)
- **DOI/arXiv:** arXiv:2510.19577
- **Notes:** Directly matches the user request; important gem5-centered exemplar.

### 3. iDSE: Navigating Design Space Exploration in High-Level Synthesis Using LLMs

- **ID:** `idse_2025`
- **Authors:** Runkai Li; Jia Xiong; Xi Wang
- **Year / Venue:** 2025 / arXiv
- **Paper type:** preprint
- **Status:** main
- **Direction:** LLM-aided HLS DSE
- **Technical route:** Natural-language/DSE reasoning; Agentic closed-loop design
- **LLM role:** LLM prunes design space, generates warm-start samples, reflects on QoR trajectories, and refines Pareto designs
- **Architecture target:** HLS directive configurations and generated microarchitectures
- **Simulator/toolchain:** vendor HLS synthesis flow; NSGA-II/ACO/MOEA-D/Lattice/HGBO-DSE baselines
- **Evaluation metrics:** 5.1x-16.6x better proximity to reference Pareto front; matches NSGA-II with 4.6% explored designs
- **PDF:** [PDF](<01_LLM_Agents_for_DSE/2025_arXiv_Li_iDSE_Navigating_Design_Space_Exploration_in_High.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2505.22086>)
- **DOI/arXiv:** arXiv:2505.22086
- **Notes:** Important HLS DSE paper; likely arXiv-only in this pass.

### 4. LLM-DSE: Searching Accelerator Parameters with LLM Agents

- **ID:** `llm_dse_2025`
- **Authors:** Hanyu Wang; Xinrui Wu; Zijian Ding; Su Zheng; Chengyue Wang; Tony Nowatzki; Yizhou Sun; Jason Cong
- **Year / Venue:** 2025 / arXiv
- **Paper type:** preprint
- **Status:** main
- **Direction:** LLM agents for accelerator/HLS DSE
- **Technical route:** Agentic closed-loop design
- **LLM role:** Router, Specialist, Arbitrator, and Critic agents guide parameter search with online verbal learning
- **Architecture target:** HLS directive/parameter optimization for domain-specific accelerators
- **Simulator/toolchain:** Merlin/Stratus/Vitis-style HLS flows; HLSyn; Rosetta
- **Evaluation metrics:** 2.55x performance gain over AutoDSE; runtime reduction; ablations on agent interactions
- **PDF:** [PDF](<01_LLM_Agents_for_DSE/2025_arXiv_Wang_LLM_DSE_Searching_Accelerator_Parameters_with_LL.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2505.12188>)
- **DOI/arXiv:** arXiv:2505.12188
- **Notes:** Strong DSE fit; accelerator/HLS rather than CPU microarchitecture.

## 02_LLM_for_Microarchitecture_Policy_Design

Microarchitecture policy design and reasoning.

### 5. Agentic Architect: An Agentic AI Framework for Architecture Design Exploration and Optimization

- **ID:** `agentic_architect_2026`
- **Authors:** Alexander Blasberg; Vasilis Kypriotis; Dimitrios Skarlatos
- **Year / Venue:** 2026 / arXiv
- **Paper type:** recent preprint
- **Status:** main; recent arXiv
- **Direction:** agentic microarchitecture design
- **Technical route:** Agentic closed-loop design
- **LLM role:** LLM agent evolves code/design policies under simulator feedback
- **Architecture target:** cache replacement; data prefetching; branch prediction
- **Simulator/toolchain:** cycle-accurate simulation; open-source agentic evaluation harness
- **Evaluation metrics:** geomean IPC speedup over LRU/Mockingjay, Bimodal/Hashed Perceptron, no-prefetch/SMS
- **PDF:** [PDF](<02_LLM_for_Microarchitecture_Policy_Design/2026_arXiv_Blasberg_Agentic_Architect_An_Agentic_AI_Framework_for_Ar.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2604.25083>)
- **DOI/arXiv:** arXiv:2604.25083
- **Notes:** Recent half-year arXiv; one of the clearest end-to-end LLM-agent microarchitecture design papers.

### 6. CacheMind: From Miss Rates to Why -- Natural-Language, Trace-Grounded Reasoning for Cache Replacement

- **ID:** `cachemind_2026`
- **Authors:** Kaushal Mhapsekar; Azam Ghanbari; Bita Aslrousta; Samira Mirbagher-Ajorpaz
- **Year / Venue:** 2026 / ASPLOS 2026 / arXiv
- **Paper type:** top conference paper / preprint
- **Status:** main; recent arXiv
- **Direction:** LLM for cache replacement reasoning
- **Technical route:** RAG/trace-grounded reasoning
- **LLM role:** Conversational RAG system explains cache traces and replacement behavior
- **Architecture target:** cache replacement
- **Simulator/toolchain:** ChampSim traces; SIEVE/RANGER retrievers
- **Evaluation metrics:** CacheMindBench accuracy: trace-grounded and policy-specific reasoning tasks
- **PDF:** [PDF](<02_LLM_for_Microarchitecture_Policy_Design/2026_ASPLOS_2026_Mhapsekar_CacheMind_From_Miss_Rates_to_Why_Natural_Languag.pdf>)
- **Official/OA:** [Official](<https://doi.org/10.1145/3779212.3790136>) / [OA](<https://arxiv.org/abs/2602.12422>)
- **DOI/arXiv:** arXiv:2602.12422; DOI:10.1145/3779212.3790136
- **Notes:** Strong match: LLM/RAG directly supports microarchitectural cache-replacement analysis.

### 7. PF-LLM: Large Language Model Hinted Hardware Prefetching

- **ID:** `pf_llm_2026`
- **Authors:** Ceyu Xu; Xiangfeng Sun; Weihang Li; Chen Bai; Bangyan Wang; Mengming Li; Zhiyao Xie; Yuan Xie
- **Year / Venue:** 2026 / ASPLOS 2026
- **Paper type:** top conference paper
- **Status:** main
- **Direction:** LLM-assisted microarchitecture policy design
- **Technical route:** LLM-assisted microarchitecture policy design
- **LLM role:** LLM hints hardware prefetching policy/design choices
- **Architecture target:** hardware prefetching / processor microarchitecture
- **Simulator/toolchain:** not available from public program page
- **Evaluation metrics:** 9.8% average IPC improvement over state-of-the-art hardware prefetching baselines on memory-intensive SPEC 2017; 18.9% over state-of-the-art ensemble methods
- **PDF:** [PDF](<02_LLM_for_Microarchitecture_Policy_Design/2026_ASPLOS_2026_Xu_PF_LLM_Large_Language_Model_Hinted_Hardware_Pref.pdf>)
- **Official/OA:** [Official](<https://doi.org/10.1145/3779212.3790202>) / [OA](<https://fact-lab.hkust.edu.hk/publications/conference-paper/2025/xu-2025-pf-llm/3779212.3790202.pdf>)
- **DOI/arXiv:** DOI:10.1145/3779212.3790202
- **Notes:** Accepted in ASPLOS 2026 Session 7D Processor Microarchitecture; ASPLOS'26 Best Paper Award. Strong top-venue microarchitecture match.

## 03_LLM_for_Simulation_Modeling_and_gem5

Architecture simulation, modeling, gem5/ChampSim workflows.

### 8. Enhancing Search-Based Testing with LLMs for Finding Bugs in System Simulators

- **ID:** `searchsys_2025`
- **Authors:** Aidan Dakhama; Karine Even-Mendoza; William B. Langdon; Hector D. Menendez; Justyna Petke
- **Year / Venue:** 2025 / Automated Software Engineering
- **Paper type:** journal article
- **Status:** main
- **Direction:** LLM-assisted architecture simulator testing
- **Technical route:** LLM for simulation workflow
- **LLM role:** Six LLMs generate structured test inputs that seed customized AFL++ mutation and differential testing
- **Architecture target:** gem5 system simulator reliability
- **Simulator/toolchain:** gem5; AFL++; SearchSYS; differential testing
- **Evaluation metrics:** 21 new gem5 bugs; 14 missimulations; 7 crashes; 101,442 issue-triggering inputs
- **PDF:** [PDF](<03_LLM_for_Simulation_Modeling_and_gem5/2025_Automated_Software_E_Dakhama_Enhancing_Search_Based_Testing_with_LLMs_for_Fin.pdf>)
- **Official/OA:** [Official](<https://doi.org/10.1007/s10515-025-00531-7>) / [OA](<https://solar.cs.ucl.ac.uk/pdf/ASE_J_Gem5_11-apr-2025.pdf>)
- **DOI/arXiv:** DOI:10.1007/s10515-025-00531-7
- **Notes:** Expanded journal version of SearchGEM5; strong simulator/tool reliability item.

### 9. SearchGEM5: Towards Reliable gem5 with Search Based Software Testing and Large Language Models

- **ID:** `searchgem5_2023`
- **Authors:** Aidan Dakhama; Karine Even-Mendoza; William B. Langdon; Hector Menendez; Justyna Petke
- **Year / Venue:** 2023 / SSBSE 2023 / LNCS
- **Paper type:** conference paper
- **Status:** main
- **Direction:** LLM-assisted architecture simulator testing
- **Technical route:** LLM for simulation workflow
- **LLM role:** ChatGPT parameterizes C programs that seed a custom AFL++ fuzzing flow
- **Architecture target:** gem5 system simulator reliability
- **Simulator/toolchain:** gem5; AFL++; differential testing
- **Evaluation metrics:** 4,005 binaries; +1000 lines test coverage; 244 divergent gem5 simulation instances
- **PDF:** [PDF](<03_LLM_for_Simulation_Modeling_and_gem5/2023_SSBSE_2023_Dakhama_SearchGEM5_Towards_Reliable_gem5_with_Search_Bas.pdf>)
- **Official/OA:** [Official](<https://doi.org/10.1007/978-3-031-48796-5_14>) / [OA](<https://solar.cs.ucl.ac.uk/pdf/Dakhama_2023_SSBSE.pdf>)
- **DOI/arXiv:** DOI:10.1007/978-3-031-48796-5_14
- **Notes:** Not an architecture design paper, but directly improves architecture simulator reliability using LLMs.

## 04_LLM_for_Performance_Analysis_and_Optimization

Performance analysis and optimization.

### 10. LOOPRAG: Enhancing Loop Transformation Optimization with Retrieval-Augmented Large Language Models

- **ID:** `looprag_2026`
- **Authors:** Yijie Zhi; Yayu Cao; Jianhua Dai; Xiaoyang Han; Jingwen Pu; Qingran Wu; Sheng Cheng; Ming Cai
- **Year / Venue:** 2026 / ASPLOS 2026
- **Paper type:** top conference paper
- **Status:** main; recent arXiv
- **Direction:** compiler optimization with RAG LLMs
- **Technical route:** Cross-layer/HPC optimization
- **LLM role:** RAG augments LLM loop-transformation optimizer
- **Architecture target:** loop transformation and performance portability; architecture-adjacent compiler optimization
- **Simulator/toolchain:** not available from public program page
- **Evaluation metrics:** not available from public program page
- **PDF:** [PDF](<04_LLM_for_Performance_Analysis_and_Optimization/2026_ASPLOS_2026_Zhi_LOOPRAG_Enhancing_Loop_Transformation_Optimizati.pdf>)
- **Official/OA:** [Official](<https://doi.org/10.1145/3779212.3790183>) / [OA](<https://arxiv.org/abs/2512.15766>)
- **DOI/arXiv:** arXiv:2512.15766; DOI:10.1145/3779212.3790183
- **Notes:** Top-venue ASPLOS item; compiler/HPC-adjacent rather than architecture design, retained due broad scope.

### 11. LPO: Discovering Missed Peephole Optimizations with Large Language Models

- **ID:** `lpo_2026`
- **Authors:** Zhenyang Xu; Hongxu Xu; Yongqiang Tian; Xintong Zhou; Chengnian Sun
- **Year / Venue:** 2026 / ASPLOS 2026
- **Paper type:** top conference paper
- **Status:** main
- **Direction:** compiler optimization discovery with LLMs
- **Technical route:** Cross-layer/HPC optimization
- **LLM role:** LLM discovers missed peephole optimizations
- **Architecture target:** compiler optimization; systems/compiler layer adjacent to architecture
- **Simulator/toolchain:** not available from public program page
- **Evaluation metrics:** not available from public program page
- **PDF:** [PDF](<04_LLM_for_Performance_Analysis_and_Optimization/2026_ASPLOS_2026_Xu_LPO_Discovering_Missed_Peephole_Optimizations_wi.pdf>)
- **Official/OA:** [Official](<https://www.asplos-conference.org/asplos2026/program/index.html>) / [OA](<https://arxiv.org/abs/2508.16125>)
- **DOI/arXiv:** arXiv:2508.16125
- **Notes:** Included as ASPLOS top-venue LLM-for-systems optimization, but not core computer architecture.

## 05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant

HLS/RTL/specification/verification when architecture-relevant.

### 12. Bench4HLS: End-to-End Evaluation of LLMs in High-Level Synthesis Code Generation

- **ID:** `bench4hls_2026`
- **Authors:** M. Zafir Sadik Khan; Kimia Zamiri Azar; Hadi Kamali
- **Year / Venue:** 2026 / arXiv
- **Paper type:** recent preprint / benchmark
- **Status:** main; recent arXiv
- **Direction:** end-to-end benchmark for LLM-generated HLS
- **Technical route:** Benchmark/dataset; hardware design/spec optimization
- **LLM role:** Benchmarks LLM-generated HLS designs through compilation, simulation, synthesis, and PPA analysis
- **Architecture target:** HLS designs from small kernels to complex accelerators
- **Simulator/toolchain:** Xilinx Vitis HLS; Catapult HLS validation; pluggable PPA API
- **Evaluation metrics:** 170 manually drafted and validated case studies; compilation, functional correctness, synthesis feasibility, PPA
- **PDF:** [PDF](<05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant/2026_arXiv_Khan_Bench4HLS_End_to_End_Evaluation_of_LLMs_in_High.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2601.19941>)
- **DOI/arXiv:** arXiv:2601.19941
- **Notes:** Recent half-year arXiv benchmark; useful to compare HLS-Eval and HLStrans.

### 13. DiffHLS: Differential Learning for High-Level Synthesis QoR Prediction with GNNs and LLM Code Embeddings

- **ID:** `diffhls_2026`
- **Authors:** Zedong Peng; Zeju Li; Qiang Xu; Jieru Zhao
- **Year / Venue:** 2026 / arXiv
- **Paper type:** recent preprint
- **Status:** main; recent arXiv
- **Direction:** LLM code embeddings for HLS QoR prediction
- **Technical route:** Surrogate/QoR prediction augmented by pretrained code LLM embeddings
- **LLM role:** Pretrained code LLM embeddings improve delta-path QoR prediction
- **Architecture target:** HLS pragma-driven design variants
- **Simulator/toolchain:** PolyBench; ForgeHLS; GNN backbones
- **Evaluation metrics:** lower MAPE than GNN baselines; LLM embeddings improve GNN-only ablation
- **PDF:** [PDF](<05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant/2026_arXiv_Peng_DiffHLS_Differential_Learning_for_High_Level_Syn.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2604.09240>)
- **DOI/arXiv:** arXiv:2604.09240
- **Notes:** Recent half-year arXiv; more prediction/surrogate than agentic design.

### 14. ChatHLS: Towards Systematic Design Automation and Optimization for High-Level Synthesis

- **ID:** `chathls_2025`
- **Authors:** Runkai Li; Jia Xiong; Xiuyuan He; Jiaqi Lv; Jieru Zhao; Qiang Xu; Xi Wang
- **Year / Venue:** 2025 / arXiv
- **Paper type:** preprint
- **Status:** main
- **Direction:** multi-agent HLS design automation
- **Technical route:** LLM for simulation workflow; hardware design/spec optimization
- **LLM role:** Fine-tuned LLMs in multi-agent framework for HLS-C debugging and QoR-aware directive optimization
- **Architecture target:** HLS code and accelerator design
- **Simulator/toolchain:** HLS toolchains; verification-oriented data augmentation
- **Evaluation metrics:** 82.7% repair pass rate; 1.9x-14.8x speedups; 4.9x geomean over DSL-based approaches
- **PDF:** [PDF](<05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant/2025_arXiv_Li_ChatHLS_Towards_Systematic_Design_Automation_and.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2507.00642>)
- **DOI/arXiv:** arXiv:2507.00642
- **Notes:** Bridge between HLS code generation, repair, and architecture optimization.

### 15. High-level Synthesis Directives Design Optimization via Large Language Model

- **ID:** `hls_directives_llm_2025`
- **Authors:** Xufeng Yao; Wenqian Zhao; Qi Sun; Cheng Zhuo; Bei Yu
- **Year / Venue:** 2025 / ACM Transactions on Design Automation of Electronic Systems
- **Paper type:** journal article
- **Status:** main
- **Direction:** LLM for HLS directive optimization
- **Technical route:** Hardware design/spec optimization; Agentic closed-loop design
- **LLM role:** Uses LLMs as feature extractors and autonomous agents for HLS directive optimization
- **Architecture target:** HLS directives and FPGA design space exploration
- **Simulator/toolchain:** HLS DSE workflow; Bayesian optimization context
- **Evaluation metrics:** HLS directive optimization quality; see journal paper for details
- **PDF:** -
- **Official/OA:** [Official](<https://doi.org/10.1145/3747291>)
- **DOI/arXiv:** DOI:10.1145/3747291
- **Notes:** Peer-reviewed ACM TODAES journal article; no open PDF found in this pass.

### 16. HLS-Eval: A Benchmark and Framework for Evaluating LLMs on High-Level Synthesis Design Tasks

- **ID:** `hls_eval_2025`
- **Authors:** Stefan Abi-Karam; Cong Hao
- **Year / Venue:** 2025 / IEEE ICLAD 2025 / arXiv
- **Paper type:** conference paper / benchmark
- **Status:** main
- **Direction:** benchmark for LLM-driven HLS design tasks
- **Technical route:** Benchmark/dataset; hardware design/spec optimization
- **LLM role:** Evaluates LLMs for HLS code generation and HLS-specific code edits targeting performance/hardware efficiency
- **Architecture target:** HLS designs for accelerators and hardware systems
- **Simulator/toolchain:** Vitis HLS; automated parallel evaluation framework
- **Evaluation metrics:** 94 unique HLS designs; parseability, compilability, runnability, synthesizability, pass@k
- **PDF:** [PDF](<05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant/2025_IEEE_ICLAD_2025_Abi_Karam_HLS_Eval_A_Benchmark_and_Framework_for_Evaluatin.pdf>)
- **Official/OA:** [Official](<https://doi.org/10.1109/ICLAD65226.2025.00021>) / [OA](<https://arxiv.org/abs/2504.12268>)
- **DOI/arXiv:** arXiv:2504.12268; DOI:10.1109/ICLAD65226.2025.00021
- **Notes:** Evaluation infrastructure rather than design optimizer, but central for measuring LLM-for-HLS progress.

### 17. HLStrans: Dataset for C-to-HLS Hardware Code Synthesis

- **ID:** `hls_trans_2025`
- **Authors:** Qingyun Zou; Nuo Chen; Yao Chen; Bingsheng He; Weng-Fai Wong
- **Year / Venue:** 2025 / OpenReview / arXiv, submitted to ICLR 2026
- **Paper type:** dataset / benchmark
- **Status:** main
- **Direction:** dataset for LLM-driven C-to-HLS synthesis
- **Technical route:** Benchmark/dataset; hardware design/spec optimization
- **LLM role:** LLMs are benchmarked and used in augmentation pipeline with MCTS/DSE
- **Architecture target:** FPGA/HLS program transformations and pragmas
- **Simulator/toolchain:** HLS synthesis annotations; testbenches; DSE pipeline
- **Evaluation metrics:** 124K+ paired C/HLS programs in initial report; retrieval/fine-tuning improves success and latency
- **PDF:** [PDF](<05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant/2025_OpenReview_Zou_HLStrans_Dataset_for_C_to_HLS_Hardware_Code_Synt.pdf>)
- **Official/OA:** [Official](<https://openreview.net/forum?id=6UaXec8aUt>) / [OA](<https://arxiv.org/abs/2507.04315>)
- **DOI/arXiv:** arXiv:2507.04315
- **Notes:** Dataset/benchmark, included because it supports LLM-for-HLS architecture workflows.

### 18. LIFT: LLM-Based Pragma Insertion for HLS via GNN Supervised Fine-Tuning

- **ID:** `lift_2025`
- **Authors:** Neha Prakriya; Zijian Ding; Yizhou Sun; Jason Cong
- **Year / Venue:** 2025 / arXiv
- **Paper type:** preprint
- **Status:** main
- **Direction:** LLM-assisted HLS pragma generation
- **Technical route:** Hardware design/spec optimization with LLM fine-tuning
- **LLM role:** Fine-tuned LLM generates performance-critical pragmas with GNN supervision
- **Architecture target:** FPGA/HLS microarchitecture transformations
- **Simulator/toolchain:** HLSyn; AutoDSE; HARP; ProGraML/LLVM IR graph supervision
- **Evaluation metrics:** 3.52x over AutoDSE; 2.16x over HARP; 66x over GPT-4o baseline
- **PDF:** [PDF](<05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant/2025_arXiv_Prakriya_LIFT_LLM_Based_Pragma_Insertion_for_HLS_via_GNN.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2504.21187>)
- **DOI/arXiv:** arXiv:2504.21187
- **Notes:** HLS rather than classic Arch venue, but highly relevant to architecture-generation workflow.

### 19. SAGE-HLS: Syntax-Aware AST-Guided LLM for High-Level Synthesis Code Generation

- **ID:** `sage_hls_2025`
- **Authors:** M. Zafir Sadik Khan; Nowfel Mashnoor; Mohammad Akyash; Kimia Zamiri Azar; Hadi Kamali
- **Year / Venue:** 2025 / arXiv
- **Paper type:** preprint
- **Status:** main
- **Direction:** syntax-aware LLM for HLS code generation
- **Technical route:** Hardware design/spec optimization
- **LLM role:** Fine-tuned LLM uses AST-guided instruction prompting and Verilog-to-C/C++ porting to improve synthesizable HLS code generation
- **Architecture target:** HLS code for FPGA/ASIC hardware generation
- **Simulator/toolchain:** semi-automated HLS evaluation; AST-guided prompting
- **Evaluation metrics:** synthesizability and functional correctness of generated HLS code
- **PDF:** [PDF](<05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant/2025_arXiv_Khan_SAGE_HLS_Syntax_Aware_AST_Guided_LLM_for_High_Le.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2508.03558>)
- **DOI/arXiv:** arXiv:2508.03558
- **Notes:** HLS code-generation item; included because it targets synthesizable hardware design rather than generic code.

### 20. TimelyHLS: LLM-Based Timing-Aware and Architecture-Specific FPGA HLS Optimization

- **ID:** `timelyhls_2025`
- **Authors:** Nowfel Mashnoor; Mohammad Akyash; Hadi Kamali; Kimia Zamiri Azar
- **Year / Venue:** 2025 / IEEE COINS 2025 / arXiv
- **Paper type:** conference paper / preprint
- **Status:** main
- **Direction:** RAG-assisted FPGA/HLS optimization
- **Technical route:** RAG/trace-grounded reasoning; hardware design/spec optimization
- **LLM role:** LLM with RAG generates and iteratively refines timing- and architecture-specific pragmas from synthesis feedback
- **Architecture target:** FPGA-specific HLS code and RTL quality
- **Simulator/toolchain:** commercial HLS toolchains; structured FPGA architecture knowledge base
- **Evaluation metrics:** up to 70% less manual tuning; up to 4x latency speedup; >50% area savings in cases
- **PDF:** [PDF](<05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant/2025_IEEE_COINS_2025_Mashnoor_TimelyHLS_LLM_Based_Timing_Aware_and_Architectur.pdf>)
- **Official/OA:** [Official](<https://doi.org/10.48550/arXiv.2507.17962>) / [OA](<https://arxiv.org/abs/2507.17962>)
- **DOI/arXiv:** arXiv:2507.17962
- **Notes:** Architecture-specific RAG knowledge base makes it more relevant than generic RTL generation.

### 21. HLSPilot: LLM-based High-Level Synthesis

- **ID:** `hlspilot_2024`
- **Authors:** Chenwei Xiong; Cheng Liu; Huawei Li; Xiaowei Li
- **Year / Venue:** 2024 / ICCAD 2024 / arXiv
- **Paper type:** top EDA conference paper / preprint
- **Status:** main
- **Direction:** LLM-enabled end-to-end HLS hardware acceleration
- **Technical route:** LLM for simulation workflow; hardware/software co-design; DSE tool use
- **LLM role:** LLM profiles software, identifies bottlenecks, retrieves HLS strategies, generates optimized HLS code, invokes DSE tooling, and helps CPU-FPGA deployment
- **Architecture target:** hybrid CPU-FPGA accelerators and HLS-generated microarchitectures
- **Simulator/toolchain:** gprof; Vitis HLS; Xilinx Alveo U280; GenHLSOptimizer; XRT
- **Evaluation metrics:** comparable to or better than manual HLS designs on real-world application benchmarks
- **PDF:** [PDF](<05_LLM_for_Hardware_Spec_RTL_Verification_when_arch_relevant/2024_ICCAD_2024_Xiong_HLSPilot_LLM_based_High_Level_Synthesis.pdf>)
- **Official/OA:** [Official](<https://doi.org/10.1145/3676536.3676781>) / [OA](<https://arxiv.org/abs/2408.06810>)
- **DOI/arXiv:** arXiv:2408.06810; DOI:10.1145/3676536.3676781
- **Notes:** Early and important LLM-for-HLS framework; bridges profiling, partitioning, HLS codegen, DSE, and deployment.

## 06_LLM_for_HPC_System_Codesign

HPC/system/software-hardware co-design.

### 22. Optimas: An Intelligent Analytics-Informed Generative AI Framework for Performance Optimization

- **ID:** `optimas_2026`
- **Authors:** Mohammad Zaeed; Tanzima Z. Islam; Vladimir Indic
- **Year / Venue:** 2026 / arXiv
- **Paper type:** recent preprint
- **Status:** main; recent arXiv
- **Direction:** LLM agents for GPU/HPC performance optimization
- **Technical route:** Cross-layer/HPC optimization
- **LLM role:** Multi-agent workflow maps performance diagnostics to literature-backed code transformations and validates execution
- **Architecture target:** NVIDIA GPU code/performance optimization
- **Simulator/toolchain:** profilers/reports; code generation; execution validation
- **Evaluation metrics:** 3,410 experiments; 100% correct code; improves performance in 98.82% experiments; 8.02%-79.09% average gains
- **PDF:** [PDF](<06_LLM_for_HPC_System_Codesign/2026_arXiv_Zaeed_Optimas_An_Intelligent_Analytics_Informed_Genera.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2604.23892>)
- **DOI/arXiv:** arXiv:2604.23892
- **Notes:** Recent LLM-agent HPC/GPU performance optimizer; architecture-adjacent rather than classic Arch venue.

### 23. SwizzlePerf: Hardware-aware LLMs for GPU Kernel Performance Optimization

- **ID:** `swizzleperf_2025`
- **Authors:** Arya Tschand; Muhammad Awad; Ryan Swann; Kesavan Ramakrishnan; Jeffrey Ma; Keith Lowery; Ganesh Dasika; Vijay Janapa Reddi
- **Year / Venue:** 2025 / arXiv
- **Paper type:** preprint
- **Status:** main
- **Direction:** hardware-aware LLMs for GPU kernel performance
- **Technical route:** Cross-layer/HPC optimization
- **LLM role:** LLM assists hardware-aware kernel performance optimization
- **Architecture target:** GPU kernels and hardware-aware code transformation
- **Simulator/toolchain:** not resolved in this pass
- **Evaluation metrics:** not resolved in this pass
- **PDF:** [PDF](<06_LLM_for_HPC_System_Codesign/2025_arXiv_Tschand_SwizzlePerf_Hardware_aware_LLMs_for_GPU_Kernel_P.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2508.20258>)
- **DOI/arXiv:** arXiv:2508.20258
- **Notes:** Mentioned in QuArch references; include as architecture-adjacent GPU performance work.

## 90_Surveys_Position_and_Vision

Surveys, benchmarks, position papers, vision papers.

### 24. Hardware Design and Verification with Large Language Models: A Scoping Review, Challenges, and Open Issues

- **ID:** `hardware_llm_scoping_2025`
- **Authors:** Meisam Abdollahi; Seyedeh Faegheh Yeganli; Mohammad (Amir) Baharloo; Amirali Baniasadi
- **Year / Venue:** 2025 / Electronics
- **Paper type:** survey
- **Status:** main
- **Direction:** survey of LLMs for hardware design and verification
- **Technical route:** Survey/vision
- **LLM role:** Reviews LLM use across specification, RTL, verification, chip architecture design, and EDA workflows
- **Architecture target:** chip architecture; RTL; verification; physical design
- **Simulator/toolchain:** survey
- **Evaluation metrics:** taxonomy and open issues
- **PDF:** -
- **Official/OA:** [Official](<https://www.mdpi.com/2079-9292/14/1/120>) / [OA](<https://www.mdpi.com/2079-9292/14/1/120/pdf>)
- **DOI/arXiv:** DOI:10.3390/electronics14010120
- **Notes:** Broad EDA/hardware survey; useful for taxonomy, not core Arch venue.

### 25. Large Processor Chip Model

- **ID:** `lpcm_2025`
- **Authors:** Kaiyan Chang; Mingzhi Chen; Yunji Chen; Zhirong Chen; Dongrui Fan; Junfeng Gong; Nan Guo; Yinhe Han; Qinfen Hao; Shuo Hou; Xuan Huang; Pengwei Jin; Changxin Ke; Cangyuan Li; Guangli Li; Huawei Li; Kuan Li; Naipeng Li; Shengwen Liang; Cheng Liu; Hongwei Liu; Jiahua Liu; Junliang Lv; Jianan Mu; Jin Qin; Bin Sun; Chenxi Wang; Duo Wang; Mingjun Wang; Ying Wang; Chenggang Wu; Peiyang Wu; Teng Wu; Xiao Xiao; Mengyao Xie; Chenwei Xiong; Ruiyuan Xu; Mingyu Yan; Xiaochun Ye; Kuai Yu; Rui Zhang; Shuoming Zhang; Jiacheng Zhao et al.
- **Year / Venue:** 2025 / arXiv / Science China Information Sciences for review
- **Paper type:** position paper
- **Status:** main
- **Direction:** LLM-driven end-to-end processor/chip design vision
- **Technical route:** Survey/vision; Agentic closed-loop design
- **LLM role:** LPCM proposes LLM/agent levels for compiler, binary translation, simulator, partitioning, DSE, RTL generation
- **Architecture target:** processor/chip architecture across software-hardware stack
- **Simulator/toolchain:** LLVM; gem5; Chisel; Verilog simulators; 3D Gaussian Splatting workload case study
- **Evaluation metrics:** case-study effectiveness; mostly roadmap/position analysis
- **PDF:** [PDF](<90_Surveys_Position_and_Vision/2025_arXiv_Chang_Large_Processor_Chip_Model.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2506.02929>)
- **DOI/arXiv:** arXiv:2506.02929
- **Notes:** Useful Chinese-led vision paper for LLM-for-architecture framing.

### 26. QuArch: A Benchmark for Evaluating LLM Reasoning in Computer Architecture

- **ID:** `quarch_2025`
- **Authors:** Shvetank Prakash; Andrew Cheng; Arya Tschand; Mark Mazumder; Varun Gohil; Jeffrey Ma; Jason Yik; Zishen Wan; Jessica Quaye; Elisavet Lydia Alvanaki; Avinash Kumar; Chandrashis Mazumdar; Tuhin Khare; Alexander Ingare; Ikechukwu Uchendu; Radhika Ghosal; Abhishek Tyagi; Chenyu Wang; Andrea Mattia Garavagno; Shuning Gu; Alicia Guo; Grace Hur; Luca Marcello Carloni; Tushar Krishna; Ankita Nayak; Amir Yazdanbakhsh; Vijay Janapa Reddi
- **Year / Venue:** 2025 / OpenReview / arXiv, submitted to ICLR 2026
- **Paper type:** benchmark / preprint
- **Status:** main
- **Direction:** LLM benchmark for computer architecture reasoning
- **Technical route:** Benchmark/dataset for architecture reasoning
- **LLM role:** Evaluates LLM architecture knowledge, analysis, design, and implementation reasoning
- **Architecture target:** processor design; memory systems; interconnection networks
- **Simulator/toolchain:** QA benchmark; LLM-as-judge and human grading
- **Evaluation metrics:** 2,671 expert-validated QA pairs; frontier model accuracy range about 34%-72%
- **PDF:** [PDF](<90_Surveys_Position_and_Vision/2025_OpenReview_Prakash_QuArch_A_Benchmark_for_Evaluating_LLM_Reasoning.pdf>)
- **Official/OA:** [Official](<https://openreview.net/forum?id=nhcz0uni55>) / [OA](<https://arxiv.org/abs/2510.22087>)
- **DOI/arXiv:** arXiv:2510.22087
- **Notes:** Not a design method, but foundational for evaluating LLMs in computer architecture.

### 27. Report for NSF Workshop on AI for Electronic Design Automation

- **ID:** `ai4eda_workshop_report_2024`
- **Authors:** Deming Chen; Vijay Ganesh; Weikai Li; Yizhou Sun
- **Year / Venue:** 2024 / NSF Workshop Report
- **Paper type:** report
- **Status:** main
- **Direction:** AI/LLM for EDA roadmap
- **Technical route:** Survey/vision
- **LLM role:** Discusses LLMs, GNNs, RL and AI methods for HLS/LLS, optimization, physical synthesis, test and verification
- **Architecture target:** EDA and hardware design flows
- **Simulator/toolchain:** workshop report
- **Evaluation metrics:** recommendations and research agenda
- **PDF:** -
- **Official/OA:** [Official](<https://ai4eda-workshop.github.io/>)
- **DOI/arXiv:** -
- **Notes:** Not strictly LLM-only; included as context for EDA/HLS technical route.

## 99_Candidates_Borderline

Borderline EDA/RTL/compiler candidates.

### 28. From English to ASIC: Hardware Implementation with Large Language Model

- **ID:** `from_english_to_asic_2024`
- **Authors:** E. Goh; M. Xiang; I. Wey; T. H. Teo
- **Year / Venue:** 2024 / arXiv
- **Paper type:** preprint
- **Status:** borderline
- **Direction:** natural-language to ASIC/RTL design
- **Technical route:** Hardware design/spec optimization
- **LLM role:** LLM maps English design intent toward hardware implementation
- **Architecture target:** ASIC/RTL implementation
- **Simulator/toolchain:** RTL/ASIC tool flow
- **Evaluation metrics:** implementation correctness/quality
- **PDF:** [PDF](<99_Candidates_Borderline/2024_arXiv_Goh_From_English_to_ASIC_Hardware_Implementation_wit.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2403.07039>)
- **DOI/arXiv:** arXiv:2403.07039
- **Notes:** Natural-language hardware implementation; kept as EDA candidate.

### 29. RTLLM: An Open-Source Benchmark for Design RTL Generation with Large Language Model

- **ID:** `rtllm_2024`
- **Authors:** Yao Lu; Shang Liu; Qijun Zhang; Zhiyao Xie
- **Year / Venue:** 2024 / ASP-DAC 2024
- **Paper type:** conference paper
- **Status:** borderline
- **Direction:** benchmark for LLM RTL generation
- **Technical route:** Benchmark/dataset; hardware design/spec optimization
- **LLM role:** Evaluates LLMs for RTL design generation
- **Architecture target:** RTL generation
- **Simulator/toolchain:** RTL design benchmark and validation flow
- **Evaluation metrics:** RTL generation benchmark pass/fail metrics
- **PDF:** -
- **Official/OA:** [Official](<https://doi.org/10.1109/ASP-DAC58780.2024.10473904>)
- **DOI/arXiv:** DOI:10.1109/ASP-DAC58780.2024.10473904
- **Notes:** Strong EDA benchmark; not architecture-specific but useful as foundation.

### 30. SpecLLM: Exploring Generation and Review of VLSI Design Specification with Large Language Model

- **ID:** `spec_llm_2024`
- **Authors:** Mingjie Li; Wenji Fang; Qijun Zhang; Zhiyao Xie
- **Year / Venue:** 2024 / arXiv
- **Paper type:** preprint
- **Status:** borderline
- **Direction:** LLM for VLSI specification generation/review
- **Technical route:** Hardware design/spec optimization
- **LLM role:** LLM generates and reviews VLSI design specifications
- **Architecture target:** VLSI/SoC design specification
- **Simulator/toolchain:** specification evaluation flow
- **Evaluation metrics:** spec generation/review quality
- **PDF:** [PDF](<99_Candidates_Borderline/2024_arXiv_Li_SpecLLM_Exploring_Generation_and_Review_of_VLSI.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2401.13266>)
- **DOI/arXiv:** arXiv:2401.13266
- **Notes:** Specification-level rather than architecture evaluation; include as borderline.

### 31. Verigen: A Large Language Model for Verilog Code Generation

- **ID:** `verigen_2024`
- **Authors:** Shailja Thakur; Baleegh Ahmad; Hammond Pearce; Benjamin Tan; Brendan Dolan-Gavitt; Ramesh Karri; Siddharth Garg
- **Year / Venue:** 2024 / ACM Transactions on Design Automation of Electronic Systems
- **Paper type:** journal article
- **Status:** borderline
- **Direction:** LLM for Verilog generation
- **Technical route:** Hardware design/spec optimization
- **LLM role:** Fine-tuned LLM generates Verilog code
- **Architecture target:** RTL code generation
- **Simulator/toolchain:** Verilog evaluation/testbench flow
- **Evaluation metrics:** Verilog generation correctness metrics
- **PDF:** [PDF](<99_Candidates_Borderline/2024_ACM_Transactions_on_Thakur_Verigen_A_Large_Language_Model_for_Verilog_Code.pdf>)
- **Official/OA:** [Official](<https://doi.org/10.1145/3643681>) / [OA](<https://arxiv.org/abs/2308.00708>)
- **DOI/arXiv:** arXiv:2308.00708; DOI:10.1145/3643681
- **Notes:** Pure RTL-generation baseline; included as borderline due EDA extension.

### 32. Advanced Language Model-Driven Verilog Development: Enhancing Power, Performance, and Area Optimization in Code Synthesis

- **ID:** `advanced_verilog_ppa_2023`
- **Authors:** Keshav Thorat; Jason Zhao; Yucheng Liu; Hengyue Peng; Xuechao Xie; Bolei Lei; Zhiru Zhang; Chao Ding
- **Year / Venue:** 2023 / arXiv
- **Paper type:** preprint
- **Status:** borderline
- **Direction:** LLM-driven Verilog PPA optimization
- **Technical route:** Hardware design/spec optimization
- **LLM role:** LLM assists Verilog code synthesis with PPA objectives
- **Architecture target:** RTL/PPA
- **Simulator/toolchain:** Verilog synthesis/evaluation flow
- **Evaluation metrics:** PPA optimization metrics
- **PDF:** [PDF](<99_Candidates_Borderline/2023_arXiv_Thorat_Advanced_Language_Model_Driven_Verilog_Developme.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2312.01022>)
- **DOI/arXiv:** arXiv:2312.01022
- **Notes:** PPA angle makes it somewhat architecture-relevant, but still mostly RTL/EDA.

### 33. ChipNeMo: Domain-Adapted LLMs for Chip Design

- **ID:** `chipnemo_2023`
- **Authors:** NVIDIA research team
- **Year / Venue:** 2023 / arXiv
- **Paper type:** preprint
- **Status:** borderline
- **Direction:** domain-adapted LLMs for chip design
- **Technical route:** Hardware design/spec optimization; RAG/assistant
- **LLM role:** Domain-adapted LLM assistant for chip-design tasks
- **Architecture target:** chip design workflows; EDA assistance
- **Simulator/toolchain:** chip-design corpora; domain adaptation; retrieval
- **Evaluation metrics:** domain task quality metrics; details in paper
- **PDF:** [PDF](<99_Candidates_Borderline/2023_arXiv_team_ChipNeMo_Domain_Adapted_LLMs_for_Chip_Design.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2311.00176>)
- **DOI/arXiv:** arXiv:2311.00176
- **Notes:** Important chip-design LLM paper, but broader EDA rather than computer architecture.

### 34. RTLCoder: Outperforming GPT-3.5 in Design RTL Generation with Our Open-Source Dataset and Lightweight Solution

- **ID:** `rtlcoder_2023`
- **Authors:** Shang Liu; Wenji Fang; Yao Lu; Qijun Zhang; Hongce Zhang; Zhiyao Xie
- **Year / Venue:** 2023 / arXiv
- **Paper type:** preprint
- **Status:** borderline
- **Direction:** LLM for RTL generation
- **Technical route:** Hardware design/spec optimization
- **LLM role:** Lightweight model/dataset for RTL design generation
- **Architecture target:** RTL generation
- **Simulator/toolchain:** RTL generation dataset/evaluation
- **Evaluation metrics:** outperforms GPT-3.5 on RTL generation tasks
- **PDF:** [PDF](<99_Candidates_Borderline/2023_arXiv_Liu_RTLCoder_Outperforming_GPT_3_5_in_Design_RTL_Gen.pdf>)
- **Official/OA:** [Official](<https://arxiv.org/abs/2312.08617>)
- **DOI/arXiv:** arXiv:2312.08617
- **Notes:** Pure RTL-generation; included as candidate.
