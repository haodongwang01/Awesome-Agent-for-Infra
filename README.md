# Awesome Agent-for-Infra

> A living survey of AI agents for designing, optimizing, serving, and benchmarking AI infrastructure.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

AI infrastructure is becoming agentic. The important systems are no longer just models that answer questions; they are agents that read specs, call compilers, run simulators, inspect profiler traces, patch code, tune deployments, and close the loop with executable evidence.

This repository organizes that landscape around four infrastructure layers. Each linked survey file uses the same three resource categories: `Skills`, `Paper`, and `Toolchain`.

## Survey Map

| Track | Core Problem | Details |
| --- | --- | --- |
| Agent for Hardware and Architecture Design | Can agents turn design intent into verified and optimized hardware artifacts under simulator, synthesis, and PPA feedback? | [Open survey](docs/hardware-architecture.md) |
| Agent for Operators, Kernels and Compilers | Can agents generate, repair, and optimize kernels or compiler transformations using compile errors, tests, profiler traces, and hardware feedback? | [Open survey](docs/operators-kernels-compilers.md) |
| Agent for Model Serving and System Optimization | Can agents tune serving engines, schedulers, deployments, and runtime configs to satisfy latency, throughput, reliability, and cost goals? | [Open survey](docs/model-serving-system-optimization.md) |
| Environments and Benchmarks | How should infra agents be evaluated with executable tasks, stable harnesses, reproducible metrics, and auditable baselines? | [Open survey](docs/environments-benchmarks.md) |

## Repository Layout

```text
docs/
  hardware-architecture.md
  operators-kernels-compilers.md
  model-serving-system-optimization.md
  environments-benchmarks.md
```

Last updated: 2026-06-18.
