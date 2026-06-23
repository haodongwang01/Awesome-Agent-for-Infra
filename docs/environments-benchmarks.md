# Environments and Benchmarks

[Back to README](../README.md)

## Core Problem

How should infrastructure agents be evaluated so that progress means real executable improvement rather than better-looking text?

This track is the measuring layer. Infra-agent benchmarks need environments where actions have consequences: code must compile, hardware must simulate, kernels must run, servers must meet SLOs, and every claimed improvement must be reproducible.



## Key Questions

- What should the agent be allowed to read, write, run, and mutate?
- Which metrics distinguish real progress from benchmark overfitting?
- How should traces, logs, generated code, configs, and hardware metadata be stored?
- How should leaderboards handle hardware differences, flaky tests, and tuning budgets?

## Paper

### Benchmarks

| Date | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-|:-:|:-:|
| 2025 Feb | `KernelBench` | GPU kernel generation benchmark with correctness and speed metrics | [![Paper][paper-badge]](https://arxiv.org/abs/2502.10517) | [![Code][code-badge]](https://github.com/ScalingIntelligence/KernelBench) |
| 2023 Oct | `SWE-bench` | Repo-level execution and patch-evaluation design for software agents | [![Paper][paper-badge]](https://arxiv.org/abs/2310.06770) [![Docs][docs-badge]](https://www.swebench.com/) | [![Code][code-badge]](https://github.com/SWE-bench/SWE-bench) |
| 2023 Sep | `VerilogEval` | HDL generation and test-driven evaluation for hardware agents | [![Paper][paper-badge]](https://arxiv.org/abs/2309.07544) | [![Code][code-badge]](https://github.com/NVlabs/verilog-eval) |
| 2019 Nov | `MLPerf Inference` | Industry-standard inference benchmarking methodology and reference workloads | [![Paper][paper-badge]](https://arxiv.org/abs/1911.02549) | [![Code][code-badge]](https://github.com/mlcommons/inference) |

## Skills

| Skill | What it should do |
| --- | --- |
| `benchmark-task-authoring` | Turn real infra workflows into executable, judgeable tasks. |
| `tool-sandbox-builder` | Define safe tool boundaries for compilers, simulators, profilers, and servers. |
| `artifact-packager` | Store code, configs, logs, traces, metrics, and environment metadata per run. |
| `failure-taxonomy-labeler` | Classify failures as syntax, semantic, timeout, regression, flaky, unsafe, or non-reproducible. |
| `leaderboard-validator` | Verify submissions under fixed hardware and software constraints. |
| `baseline-runner` | Compare agents against scripts, search methods, and expert-written baselines. |

## Toolchain

### Evaluation Toolchains

| Date | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-|:-:|:-:|
| 2023 Nov | `LLMPerf` | LLM serving benchmark harness for latency and throughput workloads | [![Blog][blog-badge]](https://www.anyscale.com/blog/reproducible-performance-metrics-for-llm-inference) | [![Code][code-badge]](https://github.com/ray-project/llmperf) |
| - | `MLPerf LoadGen` | Load generation and scenario control for inference benchmarking | [![Docs][docs-badge]](https://github.com/mlcommons/inference/tree/master/loadgen) | [![Code][code-badge]](https://github.com/mlcommons/inference/tree/master/loadgen) |
| - | `Triton Perf Analyzer` | Performance measurement tooling for inference deployments | [![Docs][docs-badge]](https://docs.nvidia.com/deeplearning/triton-inference-server/user-guide/docs/perf_analyzer/README.html) | [![Code][code-badge]](https://github.com/triton-inference-server/perf_analyzer) |
| - | `OpenAI Evals` | Evaluation framework useful for wrapping agent tasks and judges | [![Docs][docs-badge]](https://developers.openai.com/cookbook/examples/evaluation/getting_started_with_openai_evals) | [![Code][code-badge]](https://github.com/openai/evals) |
| - | `Inspect` | Evaluation framework for agentic and tool-using model assessments | [![Docs][docs-badge]](https://inspect.aisi.org.uk/) | [![Code][code-badge]](https://github.com/UKGovernmentBEIS/inspect_ai) |
| 2023 Jun | `ArchGym` | Architecture design-space environment for closed-loop optimization agents | [![Paper][paper-badge]](https://arxiv.org/abs/2306.08888) | [![Code][code-badge]](https://github.com/srivatsankrishnan/oss-arch-gym) |


[paper-badge]: https://img.shields.io/badge/-Paper-0f766e?style=flat-square
[docs-badge]: https://img.shields.io/badge/-Docs-475569?style=flat-square
[blog-badge]: https://img.shields.io/badge/-Blog-b45309?style=flat-square
[code-badge]: https://img.shields.io/badge/-Code-111827?style=flat-square&logo=github&logoColor=white
