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

## Skills

| Skill | What it should do |
| --- | --- |
| `spec-to-rtl` | Convert natural-language specs into modular RTL plus assumptions and interface contracts. |
| `rtl-compile-fix` | Run Verilator, Icarus, or Yosys logs through an agent repair loop. |
| `cocotb-testgen` | Generate directed and randomized tests from module specs. |
| `waveform-debugger` | Inspect traces and explain mismatches between expected and observed behavior. |
| `ppa-tuning-loop` | Run synthesis/PnR, parse timing-area-power reports, and propose design changes. |
| `arch-search-agent` | Explore simulator or accelerator design spaces with budgeted experiments. |

## Paper

| Paper | Why it matters |
| --- | --- |
| [ChipNeMo](https://arxiv.org/abs/2311.00176) | Domain-adapted LLMs for industrial chip design workflows such as EDA scripting and bug summarization. |
| [LLM4EDA](https://arxiv.org/abs/2401.12224) | A useful taxonomy for LLMs across HDL generation, EDA scripts, verification, and future physical-design workflows. |
| [RTLLM](https://arxiv.org/abs/2308.05345) | RTL generation benchmark with syntax, functionality, and design-quality goals. |
| [OpenLLM-RTL](https://arxiv.org/abs/2503.15112) | Extends open RTL generation and verification evaluation with RTLLM 2.0, AssertEval, and RTLCoder data. |

## Toolchain

| Toolchain | Role in the agent loop |
| --- | --- |
| [Awesome-LLM4EDA](https://github.com/Thinklab-SJTU/Awesome-LLM4EDA) | Curated index for LLM-assisted electronic design automation. |
| [VerilogEval](https://github.com/NVlabs/verilog-eval) | HDL generation benchmark and harness for test-driven correctness. |
| [OpenROAD Flow Scripts](https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts) | Open RTL-to-GDS flow for measurable physical-design feedback. |
| [Verilator](https://github.com/verilator/verilator) | Fast open-source Verilog/SystemVerilog simulation for compile-and-test loops. |
| [cocotb](https://github.com/cocotb/cocotb) | Python-based HDL verification harness that fits agent-generated tests and debuggers. |
| [Chipyard](https://github.com/ucb-bar/chipyard) | RISC-V SoC design environment for architecture and accelerator exploration. |
| [gem5](https://github.com/gem5/gem5) | Architecture simulator for CPU, memory-system, and full-system design experiments. |
| [ArchGym](https://github.com/srivatsankrishnan/oss-arch-gym) | Gym-style environment for ML-driven architecture design-space exploration. |

## Evaluation Signals

| Signal | Examples |
| --- | --- |
| Correctness | Testbench pass rate, assertions, formal checks, waveform consistency |
| Synthesizability | Verilator/Yosys/OpenROAD success, tool warnings, unsupported constructs |
| PPA | Timing, area, power, frequency, resource utilization |
| Search quality | Pareto frontier, simulator score, design-space coverage |
| Reproducibility | Tool versions, process node, target platform, seeds, workload traces |
