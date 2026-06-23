<div align="center">

## Awesome Agent-for-Infra

[![Awesome][awesome-badge]](https://github.com/sindresorhus/awesome)
[![Repository][repo-badge]](https://github.com/haodongwang01/Awesome-Agent-for-Infra)
[![License][license-badge]](LICENSE)

</div>

> We welcome issues and pull requests for missing papers, toolchains, benchmarks, and reproducible agent workflows around AI infrastructure.

## 🎉 News

- **[2026 Jun 18]** Released the initial four-track map for AI agents in infrastructure.

## 📖 Contents

- [Awesome Agent-for-Infra](#awesome-agent-for-infra)
- [🎉 News](#-news)
- [📖 Contents](#-contents)
- [🧭 Survey Map](#-survey-map)
- [📄 Resource List](#-resource-list)
  - [Hardware and Architecture Design](#hardware-and-architecture-design)
  - [Operators, Kernels and Compilers](#operators-kernels-and-compilers)
  - [Model Serving and System Optimization](#model-serving-and-system-optimization)
  - [Environments and Benchmarks](#environments-and-benchmarks)
- [🌟 Acknowledgment](#-acknowledgment)

## 🧭 Survey Map

| Track | Core Problem | Details |
|:-:|:-|:-:|
| Hardware and Architecture Design | Can agents turn design intent into verified and optimized hardware artifacts under simulator, synthesis, and PPA feedback? | [![Open][open-badge]](docs/hardware-architecture.md) |
| Operators, Kernels and Compilers | Can agents generate, repair, and optimize kernels or compiler transformations using compile errors, tests, profiler traces, and hardware feedback? | [![Open][open-badge]](docs/operators-kernels-compilers.md) |
| Model Serving and System Optimization | Can agents tune serving engines, schedulers, deployments, and runtime configs to satisfy latency, throughput, reliability, and cost goals? | [![Open][open-badge]](docs/model-serving-system-optimization.md) |
| Environments and Benchmarks | How should infra agents be evaluated with executable tasks, stable harnesses, reproducible metrics, and auditable baselines? | [![Open][open-badge]](docs/environments-benchmarks.md) |

## 📄 Resource List

### Hardware and Architecture Design

| Date | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-|:-:|:-:|
| 2025 Mar | `OpenLLM-RTL` | Open RTL generation and verification evaluation with RTLLM 2.0, AssertEval, and RTLCoder data | [![Paper][paper-badge]](https://arxiv.org/abs/2503.15112) | - |
| 2024 Jan | `LLM4EDA` | A taxonomy for LLMs across HDL generation, EDA scripts, verification, and physical-design workflows | [![Paper][paper-badge]](https://arxiv.org/abs/2401.12224) | - |
| 2023 Nov | `ChipNeMo` | Domain-adapted LLMs for industrial chip design workflows | [![Paper][paper-badge]](https://arxiv.org/abs/2311.00176) | - |
| 2023 Sep | `VerilogEval` | Evaluating large language models for Verilog code generation | [![Paper][paper-badge]](https://arxiv.org/abs/2309.07544) | [![Code][code-badge]](https://github.com/NVlabs/verilog-eval) |
| 2023 Aug | `RTLLM` | RTL generation benchmark with syntax, functionality, and design-quality goals | [![Paper][paper-badge]](https://arxiv.org/abs/2308.05345) | - |
| 2023 Jun | `ArchGym` | Open-source gymnasium for machine-learning-assisted architecture design | [![Paper][paper-badge]](https://arxiv.org/abs/2306.08888) | [![Code][code-badge]](https://github.com/srivatsankrishnan/oss-arch-gym) |
| 2019 Jun | `OpenROAD` | Open-source digital flow for RTL-to-GDS implementation | [![Paper][paper-badge]](https://vlsicad.ucsd.edu/Publications/Conferences/371/c371.pdf) [![Docs][docs-badge]](https://openroad-flow-scripts.readthedocs.io/) | [![Code][code-badge]](https://github.com/The-OpenROAD-Project/OpenROAD-flow-scripts) |

### Operators, Kernels and Compilers

| Date | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-|:-:|:-:|
| 2026 May | `KernelBench-X` | Category-aware benchmark for LLM-generated GPU kernels across task types and hardware behavior | [![Paper][paper-badge]](https://arxiv.org/abs/2605.04956) | [![Code][code-badge]](https://github.com/BonnieW05/KernelBenchX) |
| 2026 Mar | `KernelFoundry` | Hardware-aware evolutionary kernel optimization with distributed benchmarking | [![Paper][paper-badge]](https://arxiv.org/abs/2603.12440) | [![Code][code-badge]](https://github.com/isl-org/kernelfoundry) |
| 2026 Mar | `KernelSkill` | Multi-agent kernel optimization with reusable expert skills and trajectory memory | [![Paper][paper-badge]](https://arxiv.org/abs/2603.10085) | [![Code][code-badge]](https://github.com/0satan0/KernelMem) |
| 2025 Feb | `KernelBench` | Evaluates whether LLMs can write correct and faster GPU kernels for PyTorch workloads | [![Paper][paper-badge]](https://arxiv.org/abs/2502.10517) | [![Code][code-badge]](https://github.com/ScalingIntelligence/KernelBench) |
| 2023 Jun | `AlphaDev` | AI-discovered sorting algorithms, a precedent for agentic low-level optimization | [![Paper][paper-badge]](https://www.nature.com/articles/s41586-023-06004-9) | - |
| 2022 Oct | `AlphaTensor` | Reinforcement learning for discovering matrix multiplication algorithms | [![Paper][paper-badge]](https://www.nature.com/articles/s41586-022-05172-4) | - |
| 2020 Jun | `Ansor` | Search-based auto-scheduler for tensor programs | [![Paper][paper-badge]](https://arxiv.org/abs/2006.06762) | - |
| 2019 Jun | `Triton` | Intermediate language and compiler for tiled neural network computations | [![Paper][paper-badge]](https://dl.acm.org/doi/10.1145/3315508.3329973) [![Docs][docs-badge]](https://triton-lang.org/) | [![Code][code-badge]](https://github.com/triton-lang/triton) |
| 2018 Oct | `Apache TVM` | End-to-end optimizing compiler for deep learning | [![Paper][paper-badge]](https://www.usenix.org/conference/osdi18/presentation/chen) [![Docs][docs-badge]](https://tvm.apache.org/) | [![Code][code-badge]](https://github.com/apache/tvm) |
| 2017 Dec | `CUTLASS` | CUDA templates and primitives for high-performance GEMM and related kernels | [![Blog][blog-badge]](https://developer.nvidia.com/blog/cutlass-linear-algebra-cuda/) [![Docs][docs-badge]](https://docs.nvidia.com/cutlass/) | [![Code][code-badge]](https://github.com/NVIDIA/cutlass) |

### Model Serving and System Optimization

| Date | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-|:-:|:-:|
| 2024 Mar | `Sarathi-Serve` | Chunked prefill and stall-free scheduling for throughput-latency tradeoffs | [![Paper][paper-badge]](https://arxiv.org/abs/2403.02310) | [![Code][code-badge]](https://github.com/microsoft/sarathi-serve) |
| 2023 Dec | `SGLang` | Structured language model programs with runtime optimizations such as KV-cache reuse | [![Paper][paper-badge]](https://arxiv.org/abs/2312.07104) | [![Code][code-badge]](https://github.com/sgl-project/sglang) |
| 2023 Oct | `TensorRT-LLM` | NVIDIA inference stack for optimized LLM deployment | [![Blog][blog-badge]](https://developer.nvidia.com/blog/optimizing-inference-on-llms-with-tensorrt-llm-now-publicly-available/) [![Docs][docs-badge]](https://nvidia.github.io/TensorRT-LLM/) | [![Code][code-badge]](https://github.com/NVIDIA/TensorRT-LLM) |
| 2023 Sep | `vLLM` | High-throughput LLM serving with KV-cache paging and continuous batching | [![Paper][paper-badge]](https://arxiv.org/abs/2309.06180) | [![Code][code-badge]](https://github.com/vllm-project/vllm) |
| 2020 Jul | `KServe` | Kubernetes-native model serving and inference platform | [![Paper][paper-badge]](https://arxiv.org/abs/2007.07366) [![Docs][docs-badge]](https://kserve.github.io/website/) | [![Code][code-badge]](https://github.com/kserve/kserve) |
| - | `TGI` | Hugging Face serving stack for text generation workloads | [![Docs][docs-badge]](https://huggingface.co/docs/text-generation-inference) | [![Code][code-badge]](https://github.com/huggingface/text-generation-inference) |
| - | `llama.cpp` | Portable inference runtime with CPU, quantization, and edge-deployment relevance | - | [![Code][code-badge]](https://github.com/ggml-org/llama.cpp) |

### Environments and Benchmarks

| Date | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-|:-:|:-:|
| 2025 Feb | `KernelBench` | GPU kernel generation benchmark with correctness and speed metrics | [![Paper][paper-badge]](https://arxiv.org/abs/2502.10517) | [![Code][code-badge]](https://github.com/ScalingIntelligence/KernelBench) |
| 2023 Nov | `LLMPerf` | LLM serving benchmark harness for latency and throughput workloads | [![Blog][blog-badge]](https://www.anyscale.com/blog/reproducible-performance-metrics-for-llm-inference) | [![Code][code-badge]](https://github.com/ray-project/llmperf) |
| 2023 Oct | `SWE-bench` | Repo-level execution and patch-evaluation design for software agents | [![Paper][paper-badge]](https://arxiv.org/abs/2310.06770) [![Docs][docs-badge]](https://www.swebench.com/) | [![Code][code-badge]](https://github.com/SWE-bench/SWE-bench) |
| 2019 Nov | `MLPerf Inference` | Industry-standard inference benchmarking methodology and reference workloads | [![Paper][paper-badge]](https://arxiv.org/abs/1911.02549) | [![Code][code-badge]](https://github.com/mlcommons/inference) |
| - | `Triton Perf Analyzer` | Performance measurement tooling for inference deployments | [![Docs][docs-badge]](https://docs.nvidia.com/deeplearning/triton-inference-server/user-guide/docs/perf_analyzer/README.html) | [![Code][code-badge]](https://github.com/triton-inference-server/perf_analyzer) |
| - | `OpenAI Evals` | Evaluation framework useful for wrapping agent tasks and judges | [![Docs][docs-badge]](https://developers.openai.com/cookbook/examples/evaluation/getting_started_with_openai_evals) | [![Code][code-badge]](https://github.com/openai/evals) |
| - | `Inspect` | Evaluation framework for agentic and tool-using model assessments | [![Docs][docs-badge]](https://inspect.aisi.org.uk/) | [![Code][code-badge]](https://github.com/UKGovernmentBEIS/inspect_ai) |

## 🌟 Acknowledgment

This survey is built from the open papers, benchmarks, and systems maintained by the AI infrastructure community. The README structure draws inspiration from [TsinghuaC3I/Awesome-RL-for-LRMs](https://github.com/TsinghuaC3I/Awesome-RL-for-LRMs).

[awesome-badge]: https://img.shields.io/badge/Awesome-List-0f766e?style=flat-square&logo=awesome-lists&logoColor=white
[repo-badge]: https://img.shields.io/badge/Repo-Awesome--Agent--for--Infra-334155?style=flat-square&logo=github&logoColor=white
[license-badge]: https://img.shields.io/badge/License-MIT-64748b?style=flat-square
[open-badge]: https://img.shields.io/badge/-Open-475569?style=flat-square
[paper-badge]: https://img.shields.io/badge/-Paper-0f766e?style=flat-square
[docs-badge]: https://img.shields.io/badge/-Docs-475569?style=flat-square
[blog-badge]: https://img.shields.io/badge/-Blog-b45309?style=flat-square
[code-badge]: https://img.shields.io/badge/-Code-111827?style=flat-square&logo=github&logoColor=white
