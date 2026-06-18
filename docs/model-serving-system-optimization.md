# Agent for Model Serving and System Optimization

[Back to README](../README.md)

## Core Problem

Can agents tune the live system around a model so that serving quality, latency, throughput, reliability, and cost move in the right direction together?

This track covers serving engines, schedulers, batching, KV-cache management, quantization, routing, autoscaling, deployment topology, observability, and production load testing.

## Agent Loop

```text
Workload / SLO -> serving config -> deploy / run -> load test -> inspect traces -> tune -> validate
```

## Key Questions

- Can an agent choose serving engines and configurations for a workload instead of a toy prompt?
- Can it optimize TTFT, TPOT, throughput, tail latency, memory, and dollar cost together?
- Can it diagnose bottlenecks from traces, logs, GPU metrics, and load-test reports?
- Can it safely change deployment settings under SLO, budget, and reliability constraints?

## Skills

| Skill | What it should do |
| --- | --- |
| `serving-engine-selector` | Map workload shape to vLLM, SGLang, TensorRT-LLM, TGI, llama.cpp, or Triton. |
| `loadtest-and-tune` | Run load profiles, parse metrics, and suggest batching, scheduler, and cache settings. |
| `kv-cache-debugger` | Inspect memory pressure, prefix reuse, eviction, and fragmentation behavior. |
| `quantization-sweeper` | Evaluate accuracy, latency, and memory tradeoffs across quantization modes. |
| `autoscaling-slo-agent` | Tune replicas, concurrency, placement, and admission control under SLOs. |
| `trace-root-cause-agent` | Diagnose performance regressions from logs, traces, and GPU metrics. |

## Paper

| Paper | Why it matters |
| --- | --- |
| [vLLM / PagedAttention](https://arxiv.org/abs/2309.06180) | High-throughput LLM serving with KV-cache paging and continuous batching. |
| [SGLang](https://arxiv.org/abs/2312.07104) | Structured language model programs with runtime optimizations such as KV-cache reuse. |
| [Sarathi-Serve](https://arxiv.org/abs/2403.02310) | Chunked prefill and stall-free scheduling for throughput-latency tradeoffs. |

## Toolchain

| Toolchain | Role in the agent loop |
| --- | --- |
| [vLLM](https://github.com/vllm-project/vllm) | Production-facing open-source serving engine for LLM and multimodal inference. |
| [SGLang repo](https://github.com/sgl-project/sglang) | Open-source framework for efficient structured generation and serving. |
| [Sarathi-Serve repo](https://github.com/microsoft/sarathi-serve) | Open implementation of Sarathi-style serving experiments. |
| [TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM) | NVIDIA inference stack for optimized LLM deployment. |
| [Text Generation Inference](https://github.com/huggingface/text-generation-inference) | Hugging Face serving stack for text generation workloads. |
| [llama.cpp](https://github.com/ggml-org/llama.cpp) | Portable inference runtime with strong CPU, quantization, and edge-deployment relevance. |
| [Triton Inference Server](https://github.com/triton-inference-server/server) | General-purpose inference server for production deployment and benchmarking. |
| [KServe](https://github.com/kserve/kserve) | Kubernetes-native model serving and inference platform. |
| [Ray Serve](https://github.com/ray-project/ray) | Scalable Python serving framework for distributed inference applications. |
| [BentoML](https://github.com/bentoml/BentoML) | Model serving framework with deployment packaging and service APIs. |

## Evaluation Signals

| Signal | Examples |
| --- | --- |
| Latency | TTFT, TPOT, p50/p95/p99 latency, deadline miss rate |
| Throughput | Tokens/sec, requests/sec, concurrency, goodput under SLO |
| Resource use | GPU memory, SM utilization, KV-cache usage, CPU overhead |
| Reliability | Error rate, overload behavior, recovery time, admission-control behavior |
| Cost | GPU-hours, dollars/request, tokens/dollar, utilization under bursty traffic |
