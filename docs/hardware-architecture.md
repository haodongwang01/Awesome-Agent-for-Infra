# Agent for Hardware and Architecture Design

[Back to README](../README.md)

## Core Problem

Can agents turn ambiguous design intent into verified and optimized hardware artifacts under real tool feedback?

This track focuses on agents that write or repair RTL, generate tests, inspect simulator and synthesis logs, reason over waveforms, and search architecture design spaces. The goal is not only to pass unit tests, but to close timing, reduce area and power, and improve architecture-level performance.


## Key Questions

- Can an agent generate synthesizable and verifiable RTL from a natural-language spec?
- Can it repair Verilog/SystemVerilog using compiler, simulator, and waveform feedback?
- Can it optimize area, timing, power, and resource usage instead of only passing tests?
- Can architecture agents search accelerator, memory hierarchy, interconnect, or SoC design spaces?

## Paper

This section is organized by where each paper sits in the agent-for-hardware stack: surveys and roadmaps, benchmarks, RTL generation and repair, verification and debugging, HLS and architecture design, and EDA-flow or analog/physical-design agents.

### Surveys and Roadmaps

| Date | Venue | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-:|:-|:-:|:-:|
| 2025 Dec | ArXiv | `Agentic EDA` | Survey of autonomous digital chip design from RTL generation to physical design and security | [![Paper][paper-badge]](https://arxiv.org/abs/2512.23189) | - |
| 2024 Jan | ArXiv | `LLM4EDA` | Survey and taxonomy for LLMs across HDL generation, EDA scripts, verification, and physical-design workflows | [![Paper][paper-badge]](https://arxiv.org/abs/2401.12224) | - |

### Benchmarks and Evaluation

| Date | Venue | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-:|:-|:-:|:-:|
| 2026 Jun | ArXiv | `RTL-BenchLS` | Large-scale benchmark for RTL reasoning and generation with formal-equivalence checking | [![Paper][paper-badge]](https://arxiv.org/abs/2606.08976) | - |
| 2026 May | ArXiv | `AssertLLM2` | Realistic benchmark for SystemVerilog assertion generation from design specifications and buggy RTL | [![Paper][paper-badge]](https://arxiv.org/abs/2605.27472) | - |
| 2026 May | DAC 2026 | `RTL-BenchMT` | Agent-assisted maintenance framework for identifying, revising, and refreshing RTL generation benchmarks | [![Paper][paper-badge]](https://arxiv.org/abs/2605.15537) | - |
| 2026 Apr | ArXiv | `HWE-Bench` | Repository-level benchmark for LLM agents on real hardware bug-repair tasks across RTL and Chisel projects | [![Paper][paper-badge]](https://arxiv.org/abs/2604.14709) | - |
| 2025 Oct | ArXiv | `QuArch` | Benchmark for evaluating LLM knowledge and reasoning in computer architecture | [![Paper][paper-badge]](https://arxiv.org/abs/2510.22087) | - |
| 2025 Aug | MLCAD 2025 | `ArchXBench` | Complex digital-systems benchmark suite for LLM-driven RTL synthesis | [![Paper][paper-badge]](https://arxiv.org/abs/2508.06047) | - |
| 2025 Jun | ArXiv | `CVDP` | Comprehensive Verilog Design Problems benchmark for RTL generation, verification, debugging, and agentic tasks | [![Paper][paper-badge]](https://arxiv.org/abs/2506.14074) | - |
| 2025 Apr | LAD 2025 | `HLS-Eval` | Benchmark and framework for evaluating LLMs on high-level synthesis design and optimization tasks | [![Paper][paper-badge]](https://arxiv.org/abs/2504.12268) | [![Code][code-badge]](https://github.com/stefanpie/hls-eval) |
| 2025 Mar | ICCAD 2024 | `OpenLLM-RTL` | Open dataset and benchmark suite integrating RTLLM 2.0, AssertEval, and RTLCoder data | [![Paper][paper-badge]](https://arxiv.org/abs/2503.15112) | - |
| 2024 May | ArXiv | `RTL-Repo` | Benchmark for evaluating LLMs on large-scale, repository-context RTL design projects | [![Paper][paper-badge]](https://arxiv.org/abs/2405.17378) | - |
| 2023 Sep | ICCAD 2023 | `VerilogEval` | Benchmark for evaluating LLM-generated Verilog code against HDLBits-style functional tests | [![Paper][paper-badge]](https://arxiv.org/abs/2309.07544) | [![Code][code-badge]](https://github.com/NVlabs/verilog-eval) |
| 2023 Aug | ASP-DAC 2024 | `RTLLM` | RTL generation benchmark with syntax, functionality, and design-quality goals | [![Paper][paper-badge]](https://arxiv.org/abs/2308.05345) | - |

### RTL Generation and Repair Agents

| Date | Venue | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-:|:-|:-:|:-:|
| 2026 May | ArXiv | `Trace2Skill` | Verifier-guided skill evolution for long-context EDA agents on complex Verilog design tasks | [![Paper][paper-badge]](https://arxiv.org/abs/2605.21810) | - |
| 2026 May | ArXiv | `Verilog-Evolve` | Feedback-driven and skill-evolving Verilog generation using simulation, synthesis, and timing feedback | [![Paper][paper-badge]](https://arxiv.org/abs/2605.26498) | - |
| 2026 Apr | ArXiv | `VeriGraphi` | Multi-agent hierarchical RTL generation framework using spec-anchored knowledge graphs | [![Paper][paper-badge]](https://arxiv.org/abs/2604.14550) | - |
| 2026 Jan | ArXiv | `EvolVE` | Evolutionary search framework for LLM-based Verilog generation and PPA-oriented optimization | [![Paper][paper-badge]](https://arxiv.org/abs/2601.18067) | [![Code][code-badge]](https://github.com/weiber2002/ICRTL) |
| 2025 Nov | ArXiv | `ArchCraft` | Neural-symbolic framework for generating and verifying RTL projects from architectural papers | [![Paper][paper-badge]](https://arxiv.org/abs/2511.06067) | - |
| 2025 Jun | ArXiv | `Spec2RTL-Agent` | Multi-agent system for generating RTL implementations from complex specification documents through HLS-aware refinement | [![Paper][paper-badge]](https://arxiv.org/abs/2506.13905) | - |
| 2025 Apr | ArXiv (withdrawn) | `ComplexVCoder` | LLM-driven framework and benchmark for systematic generation of complex multi-module Verilog code | [![Paper][paper-badge]](https://arxiv.org/abs/2504.20653) | - |
| 2025 Jan | DATE 2025 | `HaVen` | Hallucination-mitigated Verilog generation framework aligned with HDL engineering practices | [![Paper][paper-badge]](https://arxiv.org/abs/2501.04908) | [![Code][code-badge]](https://github.com/Intelligent-Computing-Research-Group/HaVen) |
| 2024 Nov | ArXiv | `AIvril2` | EDA-aware multi-agent RTL generation framework using tool feedback to repair syntax and functional errors | [![Paper][paper-badge]](https://arxiv.org/abs/2412.04485) | - |
| 2024 Aug | AAAI 2025 | `VerilogCoder` | Autonomous Verilog coding agents with graph-based planning and AST-based waveform tracing | [![Paper][paper-badge]](https://arxiv.org/abs/2408.08927) | - |
| 2024 Jul | ArXiv | `AutoVCoder` | Open framework combining dataset generation, fine-tuning, and RAG for automated Verilog generation | [![Paper][paper-badge]](https://arxiv.org/abs/2407.18333) | - |
| 2024 Jul | ArXiv | `OriGen` | Open RTL generation framework using code-to-code augmentation and compiler-feedback self-reflection | [![Paper][paper-badge]](https://arxiv.org/abs/2407.16237) | - |
| 2024 Jul | ArXiv | `CodeV` | Instruction-tuned Verilog generation models built with multi-level summarization of existing RTL | [![Paper][paper-badge]](https://arxiv.org/abs/2407.10424) | - |
| 2024 Feb | ICML 2024 | `BetterV` | Controlled Verilog generation with discriminative guidance for synthesis and verification objectives | [![Paper][paper-badge]](https://arxiv.org/abs/2402.03375) | - |
| 2023 Dec | IEEE TCAD 2025 | `RTLCoder` | Open-source and efficient LLM-assisted RTL code generation model and data pipeline | [![Paper][paper-badge]](https://arxiv.org/abs/2312.08617) | - |
| 2023 Nov | DAC 2024 | `RTLFixer` | Agentic framework for repairing Verilog syntax errors with RAG, ReAct prompting, and compiler feedback | [![Paper][paper-badge]](https://arxiv.org/abs/2311.16543) | - |
| 2023 Aug | ACM TODAES 2024 | `VeriGen` | Fine-tuned language model for Verilog code generation | [![Paper][paper-badge]](https://arxiv.org/abs/2308.00708) | - |
| 2023 May | NeurIPS SysML Workshop 2023 | `ChipGPT` | Zero-code natural-language hardware design workflow for generating and selecting Verilog candidates | [![Paper][paper-badge]](https://arxiv.org/abs/2305.14019) | - |

### Verification, Debugging and Assertion Agents

| Date | Venue | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-:|:-|:-:|:-:|
| 2026 Jun | ArXiv | `VeriPilot` | LLM-powered Verilog debugging framework using golden models, CDFGs, and fine-grained bug localization | [![Paper][paper-badge]](https://arxiv.org/abs/2606.23759) | [![Code][code-badge]](https://github.com/YihanWn/VeriPilot) |
| 2026 Apr | ArXiv | `CoverAssert` | Iterative LLM assertion generation guided by functional coverage and syntax-semantic assertion representations | [![Paper][paper-badge]](https://arxiv.org/abs/2604.06607) | - |
| 2026 Apr | MDTS 2026 | `Assertain` | LLM-based security assertion generation from RTL analysis, CWE mapping, and threat models | [![Paper][paper-badge]](https://arxiv.org/abs/2604.01583) | - |
| 2025 Sep | ArXiv | `AssertFix` | Automated assertion repair framework that localizes RTL causes and fixes incorrect generated assertions | [![Paper][paper-badge]](https://arxiv.org/abs/2509.23972) | - |
| 2025 Jun | ArXiv | `BugGen` | Self-correcting multi-agent pipeline for synthesizing, inserting, and validating realistic RTL bugs | [![Paper][paper-badge]](https://arxiv.org/abs/2506.10501) | - |
| 2025 May | ArXiv | `Spec2Assertion` | Pre-RTL SystemVerilog assertion generation from specifications with progressive regularization | [![Paper][paper-badge]](https://arxiv.org/abs/2505.07995) | - |
| 2024 Jun | LAD 2024 | `VerilogReader` | LLM-aided hardware test generation for coverage-directed verification | [![Paper][paper-badge]](https://arxiv.org/abs/2406.04373) | - |
| 2024 May | ICCAD 2025 | `MEIC` | Iterative LLM framework for RTL syntax and functional debugging | [![Paper][paper-badge]](https://arxiv.org/abs/2405.06840) | - |
| 2023 Oct | FCCM 2025 | `LLM4DV` | LLM framework for interactive hardware test-stimuli generation | [![Paper][paper-badge]](https://arxiv.org/abs/2310.04535) | - |

### HLS, Processor and Accelerator Design Agents

| Date | Venue | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-:|:-|:-:|:-:|
| 2026 May | ArXiv | `Design Conductor 2.0` | Autonomous multi-agent system that builds a TurboQuant inference accelerator from paper-level input | [![Paper][paper-badge]](https://arxiv.org/abs/2605.05170) | - |
| 2026 Mar | ArXiv | `Design Conductor` | Autonomous agent that builds a Linux-capable RISC-V CPU from specification to verified layout | [![Paper][paper-badge]](https://arxiv.org/abs/2603.08716) | - |
| 2026 Jan | DATE 2026 | `Bench4HLS` | End-to-end benchmark for LLM-generated high-level synthesis designs with compilation, simulation, and PPA hooks | [![Paper][paper-badge]](https://arxiv.org/abs/2601.19941) | - |
| 2025 Jul | ACL 2026 | `ChatHLS` | Multi-agent HLS design automation and optimization workflow with error correction and design reasoning | [![Paper][paper-badge]](https://arxiv.org/abs/2507.00642) | - |
| 2025 Jun | ArXiv | `QiMeng` | Fully automated hardware and software design system for processor chips with dedicated hardware and software agents | [![Paper][paper-badge]](https://arxiv.org/abs/2506.05007) | - |
| 2025 May | ArXiv | `QiMeng-CPU-v2` | Automated superscalar processor design using learned inter-instruction data-dependency structures | [![Paper][paper-badge]](https://arxiv.org/abs/2505.03195) | - |
| 2024 Aug | ArXiv | `HLSPilot` | LLM-enabled high-level synthesis framework for application acceleration on CPU-FPGA platforms | [![Paper][paper-badge]](https://arxiv.org/abs/2408.06810) | - |
| 2023 Sep | ICCAD 2023 | `GPT4AIGChip` | LLM-powered AI accelerator design automation via natural-language prompts and demo-augmented in-context learning | [![Paper][paper-badge]](https://arxiv.org/abs/2309.10730) | - |
| 2023 Jun | ISCA 2023 | `ArchGym` | Open-source gymnasium for machine-learning-assisted architecture design-space exploration | [![Paper][paper-badge]](https://arxiv.org/abs/2306.08888) | [![Code][code-badge]](https://github.com/srivatsankrishnan/oss-arch-gym) |

### EDA Flow, Physical Design and Analog Agents

| Date | Venue | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-:|:-|:-:|:-:|
| 2026 Mar | ArXiv | `AnalogAgent` | Self-improving multi-agent framework with memory for analog circuit design automation | [![Paper][paper-badge]](https://arxiv.org/abs/2603.23910) | - |
| 2025 Aug | ArXiv | `AnalogCoder-Pro` | Multimodal LLM framework unifying analog circuit topology generation and sizing optimization | [![Paper][paper-badge]](https://arxiv.org/abs/2508.02518) | - |
| 2024 Dec | ArXiv | `AiEDA` | Agentic AI design framework for digital ASIC system design from concept toward GDSII | [![Paper][paper-badge]](https://arxiv.org/abs/2412.09745) | - |
| 2024 Jun | IEEE TCAD 2025 | `LayoutCopilot` | LLM-powered multi-agent collaborative framework for interactive analog layout design | [![Paper][paper-badge]](https://arxiv.org/abs/2406.18873) | - |
| 2024 May | AAAI 2025 | `AnalogCoder` | Training-free LLM agent for analog circuit design through Python code generation and simulation feedback | [![Paper][paper-badge]](https://arxiv.org/abs/2405.14918) | - |
| 2023 Nov | ArXiv | `ChipNeMo` | Domain-adapted LLMs for industrial chip design tasks such as EDA scripting and bug summarization | [![Paper][paper-badge]](https://arxiv.org/abs/2311.00176) | - |
| 2023 Aug | IEEE TCAD 2024 | `ChatEDA` | Autonomous EDA agent that decomposes RTL-to-GDSII tasks and generates executable EDA scripts | [![Paper][paper-badge]](https://arxiv.org/abs/2308.10204) | - |

## Skills

| Skill | What it should do |
| --- | --- |
| `spec-to-rtl` | Convert natural-language specs into modular RTL plus assumptions and interface contracts. |
| `rtl-compile-fix` | Run Verilator, Icarus, or Yosys logs through an agent repair loop. |
| `cocotb-testgen` | Generate directed and randomized tests from module specs. |
| `waveform-debugger` | Inspect traces and explain mismatches between expected and observed behavior. |
| `ppa-tuning-loop` | Run synthesis/PnR, parse timing-area-power reports, and propose design changes. |
| `arch-search-agent` | Explore simulator or accelerator design spaces with budgeted experiments. |

## Toolchain

### Toolchains and References

| Date | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-|:-:|:-:|
| - | `Awesome-LLM4EDA` | Curated index for LLM-assisted electronic design automation | - | [![Code][code-badge]](https://github.com/Thinklab-SJTU/Awesome-LLM4EDA) |
| 2019 Jun | `OpenROAD` | Open-source digital flow for RTL-to-GDS implementation | [![Paper][paper-badge]](https://vlsicad.ucsd.edu/Publications/Conferences/371/c371.pdf) [![Docs][docs-badge]](https://openroad-flow-scripts.readthedocs.io/) | [![Code][code-badge]](https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts) |
| - | `Verilator` | Fast open-source Verilog/SystemVerilog simulation for compile-and-test loops | [![Docs][docs-badge]](https://verilator.org/guide/latest/) | [![Code][code-badge]](https://github.com/verilator/verilator) |
| - | `cocotb` | Python-based HDL verification harness for agent-generated tests and debuggers | [![Docs][docs-badge]](https://docs.cocotb.org/) | [![Code][code-badge]](https://github.com/cocotb/cocotb) |
| - | `Chipyard` | RISC-V SoC design environment for architecture and accelerator exploration | [![Docs][docs-badge]](https://chipyard.readthedocs.io/) | [![Code][code-badge]](https://github.com/ucb-bar/chipyard) |
| - | `gem5` | Architecture simulator for CPU, memory-system, and full-system design experiments | [![Docs][docs-badge]](https://www.gem5.org/documentation/) | [![Code][code-badge]](https://github.com/gem5/gem5) |

## Evaluation Signals

| Signal | Examples |
| --- | --- |
| Correctness | Testbench pass rate, assertions, formal checks, waveform consistency |
| Synthesizability | Verilator/Yosys/OpenROAD success, tool warnings, unsupported constructs |
| PPA | Timing, area, power, frequency, resource utilization |
| Search quality | Pareto frontier, simulator score, design-space coverage |
| Reproducibility | Tool versions, process node, target platform, seeds, workload traces |

[paper-badge]: https://img.shields.io/badge/-Paper-0f766e?style=flat-square
[docs-badge]: https://img.shields.io/badge/-Docs-475569?style=flat-square
[code-badge]: https://img.shields.io/badge/-Code-111827?style=flat-square&logo=github&logoColor=white
