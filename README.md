<div align="center">

<img src="figs/agent-for-infra-teaser.svg" alt="Agent-for-Infra overview" style="width: 88%;"/>

## Awesome Agent-for-Infra

[![Awesome](https://img.shields.io/badge/Awesome-0066CC?style=for-the-badge&logo=awesome-lists&logoColor=white)](https://github.com/sindresorhus/awesome)
[![Survey](https://img.shields.io/badge/Survey-Agent--for--Infra-A42C25?style=for-the-badge&logo=readthedocs&logoColor=white)](#overview)
[![Github](https://img.shields.io/badge/Awesome--Agent--for--Infra-000000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/haodongwang01/Awesome-Agent-for-Infra)
[![License](https://img.shields.io/badge/License-MIT-FFD14D?style=for-the-badge)](LICENSE)

</div>

> We welcome issues and pull requests for missing papers, toolchains, benchmarks, and reproducible agent workflows around AI infrastructure.

## 🎉 News

- **[2026-06-23]** Restyled the README into a survey-style Awesome list with badges, an overview map, and categorized resource tables.
- **[2026-06-18]** Released the initial four-track map for AI agents in infrastructure.

## 📖 Contents

- [Awesome Agent-for-Infra](#awesome-agent-for-infra)
- [🎉 News](#-news)
- [📖 Contents](#-contents)
- [🗺️ Overview](#overview)
- [🧭 Survey Map](#-survey-map)
- [📄 Resource List](#-resource-list)
  - [Hardware and Architecture Design](#hardware-and-architecture-design)
  - [Operators, Kernels and Compilers](#operators-kernels-and-compilers)
  - [Model Serving and System Optimization](#model-serving-and-system-optimization)
  - [Environments and Benchmarks](#environments-and-benchmarks)
- [🌟 Acknowledgment](#-acknowledgment)
- [✨ Star History](#-star-history)

<a id="overview"></a>

## 🗺️ Overview

AI infrastructure is becoming agentic. The important systems are no longer just models that answer questions; they are agents that read specs, call compilers, run simulators, inspect profiler traces, patch code, tune deployments, and close the loop with executable evidence.

We organize the survey into four infrastructure layers:

1. <u>Hardware and Architecture Design:</u> agents that generate RTL, debug waveforms, run synthesis, and search architecture design spaces.
2. <u>Operators, Kernels and Compilers:</u> agents that generate, repair, profile, and optimize kernels, tensor programs, and compiler passes.
3. <u>Model Serving and System Optimization:</u> agents that tune serving engines, schedulers, routing, autoscaling, and deployment settings.
4. <u>Environments and Benchmarks:</u> executable harnesses and metrics for judging whether infra agents create real improvements.

## 🧭 Survey Map

| Track | Core Problem | Details |
|:-:|:-|:-:|
| Hardware and Architecture Design | Can agents turn design intent into verified and optimized hardware artifacts under simulator, synthesis, and PPA feedback? | [![Open](https://img.shields.io/badge/Open-0066CC?style=for-the-badge)](docs/hardware-architecture.md) |
| Operators, Kernels and Compilers | Can agents generate, repair, and optimize kernels or compiler transformations using compile errors, tests, profiler traces, and hardware feedback? | [![Open](https://img.shields.io/badge/Open-0066CC?style=for-the-badge)](docs/operators-kernels-compilers.md) |
| Model Serving and System Optimization | Can agents tune serving engines, schedulers, deployments, and runtime configs to satisfy latency, throughput, reliability, and cost goals? | [![Open](https://img.shields.io/badge/Open-0066CC?style=for-the-badge)](docs/model-serving-system-optimization.md) |
| Environments and Benchmarks | How should infra agents be evaluated with executable tasks, stable harnesses, reproducible metrics, and auditable baselines? | [![Open](https://img.shields.io/badge/Open-0066CC?style=for-the-badge)](docs/environments-benchmarks.md) |

## 📄 Resource List

### Hardware and Architecture Design

| Date | Name | Title | Paper / Docs | Github |
|:-:|:-:|:-|:-:|:-:|
| 2025-03 | `OpenLLM-RTL` | Open RTL generation and verification evaluation with RTLLM 2.0, AssertEval, and RTLCoder data | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2503.15112) | - |
| 2024-01 | `LLM4EDA` | A taxonomy for LLMs across HDL generation, EDA scripts, verification, and physical-design workflows | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2401.12224) | - |
| 2023-11 | `ChipNeMo` | Domain-adapted LLMs for industrial chip design workflows | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2311.00176) | - |
| 2023-08 | `RTLLM` | RTL generation benchmark with syntax, functionality, and design-quality goals | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2308.05345) | - |
| - | `VerilogEval` | HDL generation benchmark and harness for test-driven correctness | - | [![GitHub Stars](https://img.shields.io/github/stars/NVlabs/verilog-eval?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/NVlabs/verilog-eval) |
| - | `OpenROAD` | Open RTL-to-GDS flow for measurable physical-design feedback | - | [![GitHub Stars](https://img.shields.io/github/stars/The-OpenROAD-Project/OpenROAD-flow-scripts?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts) |
| - | `ArchGym` | Gym-style environment for architecture design-space exploration | - | [![GitHub Stars](https://img.shields.io/github/stars/srivatsankrishnan/oss-arch-gym?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/srivatsankrishnan/oss-arch-gym) |

### Operators, Kernels and Compilers

| Date | Name | Title | Paper / Docs | Github |
|:-:|:-:|:-|:-:|:-:|
| 2026-05 | `KernelBench-X` | Category-aware benchmark for LLM-generated GPU kernels across task types and hardware behavior | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.04956) | - |
| 2026-03 | `KernelFoundry` | Hardware-aware evolutionary kernel optimization with distributed benchmarking | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2603.12440) | - |
| 2026-03 | `KernelSkill` | Multi-agent kernel optimization with reusable expert skills and trajectory memory | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2603.10085) | - |
| 2025-02 | `KernelBench` | Evaluates whether LLMs can write correct and faster GPU kernels for PyTorch workloads | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2502.10517) | - |
| 2023-06 | `AlphaDev` | AI-discovered sorting algorithms, a precedent for agentic low-level optimization | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge)](https://www.nature.com/articles/s41586-023-06004-9) | - |
| 2022-10 | `AlphaTensor` | Reinforcement learning for discovering matrix multiplication algorithms | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge)](https://www.nature.com/articles/s41586-022-05172-4) | - |
| 2020-06 | `Ansor` | Search-based auto-scheduler for tensor programs | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2006.06762) | - |
| - | `Triton` | Python-like DSL and compiler for writing efficient GPU kernels | [![Docs](https://img.shields.io/badge/docs-1F4E79?style=for-the-badge)](https://triton-lang.org/) | [![GitHub Stars](https://img.shields.io/github/stars/triton-lang/triton?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/triton-lang/triton) |
| - | `Apache TVM` | Tensor compiler stack with auto-scheduling and hardware-aware optimization workflows | [![Docs](https://img.shields.io/badge/docs-1F4E79?style=for-the-badge)](https://tvm.apache.org/) | [![GitHub Stars](https://img.shields.io/github/stars/apache/tvm?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/apache/tvm) |
| - | `CUTLASS` | CUDA templates and primitives for high-performance GEMM and related kernels | [![Docs](https://img.shields.io/badge/docs-1F4E79?style=for-the-badge)](https://docs.nvidia.com/cutlass/) | [![GitHub Stars](https://img.shields.io/github/stars/NVIDIA/cutlass?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/NVIDIA/cutlass) |

### Model Serving and System Optimization

| Date | Name | Title | Paper / Docs | Github |
|:-:|:-:|:-|:-:|:-:|
| 2024-03 | `Sarathi-Serve` | Chunked prefill and stall-free scheduling for throughput-latency tradeoffs | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2403.02310) | [![GitHub Stars](https://img.shields.io/github/stars/microsoft/sarathi-serve?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/microsoft/sarathi-serve) |
| 2023-12 | `SGLang` | Structured language model programs with runtime optimizations such as KV-cache reuse | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2312.07104) | [![GitHub Stars](https://img.shields.io/github/stars/sgl-project/sglang?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/sgl-project/sglang) |
| 2023-09 | `vLLM` | High-throughput LLM serving with KV-cache paging and continuous batching | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2309.06180) | [![GitHub Stars](https://img.shields.io/github/stars/vllm-project/vllm?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/vllm-project/vllm) |
| - | `TensorRT-LLM` | NVIDIA inference stack for optimized LLM deployment | [![Docs](https://img.shields.io/badge/docs-1F4E79?style=for-the-badge)](https://nvidia.github.io/TensorRT-LLM/) | [![GitHub Stars](https://img.shields.io/github/stars/NVIDIA/TensorRT-LLM?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/NVIDIA/TensorRT-LLM) |
| - | `TGI` | Hugging Face serving stack for text generation workloads | [![Docs](https://img.shields.io/badge/docs-1F4E79?style=for-the-badge)](https://huggingface.co/docs/text-generation-inference) | [![GitHub Stars](https://img.shields.io/github/stars/huggingface/text-generation-inference?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/huggingface/text-generation-inference) |
| - | `llama.cpp` | Portable inference runtime with CPU, quantization, and edge-deployment relevance | - | [![GitHub Stars](https://img.shields.io/github/stars/ggml-org/llama.cpp?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/ggml-org/llama.cpp) |
| - | `KServe` | Kubernetes-native model serving and inference platform | [![Docs](https://img.shields.io/badge/docs-1F4E79?style=for-the-badge)](https://kserve.github.io/website/) | [![GitHub Stars](https://img.shields.io/github/stars/kserve/kserve?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/kserve/kserve) |

### Environments and Benchmarks

| Date | Name | Title | Paper / Docs | Github |
|:-:|:-:|:-|:-:|:-:|
| 2025-02 | `KernelBench` | GPU kernel generation benchmark with correctness and speed metrics | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2502.10517) | - |
| 2019-11 | `MLPerf Inference` | Industry-standard inference benchmarking methodology and reference workloads | [![Paper](https://img.shields.io/badge/paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/1911.02549) | [![GitHub Stars](https://img.shields.io/github/stars/mlcommons/inference?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/mlcommons/inference) |
| - | `SWE-bench` | Repo-level execution and patch-evaluation design for software agents | [![Docs](https://img.shields.io/badge/docs-1F4E79?style=for-the-badge)](https://www.swebench.com/) | [![GitHub Stars](https://img.shields.io/github/stars/SWE-bench/SWE-bench?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/SWE-bench/SWE-bench) |
| - | `LLMPerf` | LLM serving benchmark harness for latency and throughput workloads | - | [![GitHub Stars](https://img.shields.io/github/stars/ray-project/llmperf?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/ray-project/llmperf) |
| - | `Triton Perf Analyzer` | Performance measurement tooling for inference deployments | [![Docs](https://img.shields.io/badge/docs-1F4E79?style=for-the-badge)](https://docs.nvidia.com/deeplearning/triton-inference-server/user-guide/docs/perf_analyzer/README.html) | [![GitHub Stars](https://img.shields.io/github/stars/triton-inference-server/perf_analyzer?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/triton-inference-server/perf_analyzer) |
| - | `OpenAI Evals` | Evaluation framework useful for wrapping agent tasks and judges | - | [![GitHub Stars](https://img.shields.io/github/stars/openai/evals?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/openai/evals) |
| - | `Inspect` | Evaluation framework for agentic and tool-using model assessments | [![Docs](https://img.shields.io/badge/docs-1F4E79?style=for-the-badge)](https://inspect.aisi.org.uk/) | [![GitHub Stars](https://img.shields.io/github/stars/UKGovernmentBEIS/inspect_ai?style=for-the-badge&logo=github&label=GitHub&color=black)](https://github.com/UKGovernmentBEIS/inspect_ai) |

## 🌟 Acknowledgment

This survey is built from the open papers, benchmarks, and systems maintained by the AI infrastructure community. The README structure draws inspiration from [TsinghuaC3I/Awesome-RL-for-LRMs](https://github.com/TsinghuaC3I/Awesome-RL-for-LRMs).

## ✨ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=haodongwang01/Awesome-Agent-for-Infra&type=Date)](https://www.star-history.com/#haodongwang01/Awesome-Agent-for-Infra&Date)
