# Environments and Benchmarks

[Back to README](../README.md)

## Core Problem

How should infrastructure agents be evaluated so that progress means real executable improvement rather than better-looking text?

This track is the measuring layer. Infra-agent benchmarks need environments where actions have consequences: code must compile, hardware must simulate, kernels must run, servers must meet SLOs, and every claimed improvement must be reproducible.

## Evaluation Loop

```text
Task -> tool sandbox -> agent action -> execution harness -> judge -> metrics -> artifacts
```

## Key Questions

- What should the agent be allowed to read, write, run, and mutate?
- Which metrics distinguish real progress from benchmark overfitting?
- How should traces, logs, generated code, configs, and hardware metadata be stored?
- How should leaderboards handle hardware differences, flaky tests, and tuning budgets?

## Skills

| Skill | What it should do |
| --- | --- |
| `benchmark-task-authoring` | Turn real infra workflows into executable, judgeable tasks. |
| `tool-sandbox-builder` | Define safe tool boundaries for compilers, simulators, profilers, and servers. |
| `artifact-packager` | Store code, configs, logs, traces, metrics, and environment metadata per run. |
| `failure-taxonomy-labeler` | Classify failures as syntax, semantic, timeout, regression, flaky, unsafe, or non-reproducible. |
| `leaderboard-validator` | Verify submissions under fixed hardware and software constraints. |
| `baseline-runner` | Compare agents against scripts, search methods, and expert-written baselines. |

## Paper

| Paper | Why it matters |
| --- | --- |
| [MLPerf Inference](https://arxiv.org/abs/1911.02549) | Industry-standard inference benchmarking methodology and reference workloads. |
| [KernelBench](https://arxiv.org/abs/2502.10517) | GPU kernel generation benchmark with correctness and speed metrics. |
| [VerilogEval](https://github.com/NVlabs/verilog-eval) | HDL generation and test-driven evaluation for hardware agents. |
| [SWE-bench](https://github.com/SWE-bench/SWE-bench) | Software-agent benchmark that informs repo-level execution and patch-evaluation design. |

## Toolchain

| Toolchain | Role in the evaluation loop |
| --- | --- |
| [MLPerf Inference repo](https://github.com/mlcommons/inference) | Reference implementations and rules for reproducible inference evaluation. |
| [MLPerf LoadGen](https://github.com/mlcommons/inference/tree/master/loadgen) | Load generation and scenario control for inference benchmarking. |
| [LLMPerf](https://github.com/ray-project/llmperf) | LLM serving benchmark harness for latency and throughput workloads. |
| [Triton Perf Analyzer](https://github.com/triton-inference-server/perf_analyzer) | Performance measurement tooling for inference deployments. |
| [OpenAI Evals](https://github.com/openai/evals) | General evaluation framework useful for wrapping agent tasks and judges. |
| [Inspect](https://github.com/UKGovernmentBEIS/inspect_ai) | Evaluation framework for agentic and tool-using model assessments. |
| [ArchGym](https://github.com/srivatsankrishnan/oss-arch-gym) | Architecture design-space environment for closed-loop optimization agents. |
| [VerilogEval](https://github.com/NVlabs/verilog-eval) | HDL generation and test harness for hardware agents. |
| [KernelBench](https://arxiv.org/abs/2502.10517) | GPU kernel generation benchmark with correctness and speed metrics. |

## Benchmark Dimensions

| Dimension | Hardware | Kernels / compilers | Serving |
| --- | --- | --- | --- |
| Correctness | Testbench pass rate, formal checks | Numerical tolerance, shape coverage | API correctness, output constraints |
| Performance | Frequency, latency, area, power | Runtime, bandwidth, occupancy | TTFT, TPOT, throughput, tail latency |
| Cost | Tool runtime, synthesis time | Compile time, tuning budget | GPU-hours, dollars/request |
| Robustness | Spec ambiguity, corner cases | Dtype, size, architecture shifts | Traffic bursts, long context, failures |
| Reproducibility | Tool versions, seeds, targets | Hardware, drivers, compiler flags | Model, engine, workload trace |
