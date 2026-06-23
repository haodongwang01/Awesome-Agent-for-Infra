# Agent for Hardware and Architecture Design

[Back to README](../README.md)

## Core Problem

Can agents turn ambiguous design intent into verified and optimized hardware artifacts under real tool feedback?

This track focuses on agents that write or repair RTL, generate tests, inspect simulator and synthesis logs, reason over waveforms, and search architecture design spaces. The goal is not only to pass unit tests, but to close timing, reduce area and power, and improve architecture-level performance.

## Agent Loop

```text
Spec -> RTL / architecture candidate -> simulate -> debug -> synthesize -> analyze PPA -> refine
```

## Key Questions

- Can an agent generate synthesizable and verifiable RTL from a natural-language spec?
- Can it repair Verilog/SystemVerilog using compiler, simulator, and waveform feedback?
- Can it optimize area, timing, power, and resource usage instead of only passing tests?
- Can architecture agents search accelerator, memory hierarchy, interconnect, or SoC design spaces?

## Paper

### Papers and Benchmarks

| Date | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-|:-:|:-:|
| 2025 Mar | `OpenLLM-RTL` | Open RTL generation and verification evaluation with RTLLM 2.0, AssertEval, and RTLCoder data | [![Paper][paper-badge]](https://arxiv.org/abs/2503.15112) | - |
| 2024 Jan | `LLM4EDA` | A taxonomy for LLMs across HDL generation, EDA scripts, verification, and physical-design workflows | [![Paper][paper-badge]](https://arxiv.org/abs/2401.12224) | - |
| 2023 Nov | `ChipNeMo` | Domain-adapted LLMs for industrial chip design workflows such as EDA scripting and bug summarization | [![Paper][paper-badge]](https://arxiv.org/abs/2311.00176) | - |
| 2023 Sep | `VerilogEval` | Evaluating large language models for Verilog code generation | [![Paper][paper-badge]](https://arxiv.org/abs/2309.07544) | [![Code][code-badge]](https://github.com/NVlabs/verilog-eval) |
| 2023 Aug | `RTLLM` | RTL generation benchmark with syntax, functionality, and design-quality goals | [![Paper][paper-badge]](https://arxiv.org/abs/2308.05345) | - |
| 2023 Jun | `ArchGym` | Open-source gymnasium for machine-learning-assisted architecture design | [![Paper][paper-badge]](https://arxiv.org/abs/2306.08888) | [![Code][code-badge]](https://github.com/srivatsankrishnan/oss-arch-gym) |

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
