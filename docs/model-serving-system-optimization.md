# Agent for Model Serving and System Optimization

[Back to README](../README.md)

## Core Problem

Can agents tune the live system around a model so that serving quality, latency, throughput, reliability, and cost move in the right direction together?

This track covers serving engines, schedulers, batching, KV-cache management, quantization, routing, autoscaling, deployment topology, observability, and production load testing.



## Key Questions

- Can an agent choose serving engines and configurations for a workload instead of a toy prompt?
- Can it optimize TTFT, TPOT, throughput, tail latency, memory, and dollar cost together?
- Can it diagnose bottlenecks from traces, logs, GPU metrics, and load-test reports?
- Can it safely change deployment settings under SLO, budget, and reliability constraints?

## Paper

### Serving Systems and Papers

| Date | Venue | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-:|:-|:-:|:-:|
| 2024 Mar | ArXiv | `Sarathi-Serve` | Chunked prefill and stall-free scheduling for throughput-latency tradeoffs | [![Paper][paper-badge]](https://arxiv.org/abs/2403.02310) | [![Code][code-badge]](https://github.com/microsoft/sarathi-serve) |
| 2023 Dec | ArXiv | `SGLang` | Structured language model programs with runtime optimizations such as KV-cache reuse | [![Paper][paper-badge]](https://arxiv.org/abs/2312.07104) | [![Code][code-badge]](https://github.com/sgl-project/sglang) |
| 2023 Oct | NVIDIA Blog/Docs | `TensorRT-LLM` | NVIDIA inference stack for optimized LLM deployment | [![Blog][blog-badge]](https://developer.nvidia.com/blog/optimizing-inference-on-llms-with-tensorrt-llm-now-publicly-available/) [![Docs][docs-badge]](https://nvidia.github.io/TensorRT-LLM/) | [![Code][code-badge]](https://github.com/NVIDIA/TensorRT-LLM) |
| 2023 Sep | SOSP 2023 | `vLLM` | High-throughput LLM serving with KV-cache paging and continuous batching | [![Paper][paper-badge]](https://arxiv.org/abs/2309.06180) | [![Code][code-badge]](https://github.com/vllm-project/vllm) |
| 2020 Jul | ICML Workshop 2020 | `KServe` | Kubernetes-native model serving and inference platform | [![Paper][paper-badge]](https://arxiv.org/abs/2007.07366) [![Docs][docs-badge]](https://kserve.github.io/website/) | [![Code][code-badge]](https://github.com/kserve/kserve) |
| - | Docs | `TGI` | Hugging Face serving stack for text generation workloads | [![Docs][docs-badge]](https://huggingface.co/docs/text-generation-inference) | [![Code][code-badge]](https://github.com/huggingface/text-generation-inference) |
| - | - | `llama.cpp` | Portable inference runtime with CPU, quantization, and edge-deployment relevance | - | [![Code][code-badge]](https://github.com/ggml-org/llama.cpp) |

## Skills

| Skill | What it should do |
| --- | --- |
| `serving-engine-selector` | Map workload shape to vLLM, SGLang, TensorRT-LLM, TGI, llama.cpp, or Triton. |
| `loadtest-and-tune` | Run load profiles, parse metrics, and suggest batching, scheduler, and cache settings. |
| `kv-cache-debugger` | Inspect memory pressure, prefix reuse, eviction, and fragmentation behavior. |
| `quantization-sweeper` | Evaluate accuracy, latency, and memory tradeoffs across quantization modes. |
| `autoscaling-slo-agent` | Tune replicas, concurrency, placement, and admission control under SLOs. |
| `trace-root-cause-agent` | Diagnose performance regressions from logs, traces, and GPU metrics. |

## Toolchain

### Toolchains

| Date | Name | Title | Paper / Docs | Code |
|:-:|:-:|:-|:-:|:-:|
| - | `Triton Inference Server` | General-purpose inference server for production deployment and benchmarking | [![Docs][docs-badge]](https://docs.nvidia.com/deeplearning/triton-inference-server/user-guide/docs/) | [![Code][code-badge]](https://github.com/triton-inference-server/server) |
| - | `Ray Serve` | Scalable Python serving framework for distributed inference applications | [![Docs][docs-badge]](https://docs.ray.io/en/latest/serve/) | [![Code][code-badge]](https://github.com/ray-project/ray) |
| - | `BentoML` | Model serving framework with deployment packaging and service APIs | [![Docs][docs-badge]](https://docs.bentoml.com/) | [![Code][code-badge]](https://github.com/bentoml/BentoML) |


[paper-badge]: https://img.shields.io/badge/-Paper-0f766e?style=flat-square
[docs-badge]: https://img.shields.io/badge/-Docs-475569?style=flat-square
[blog-badge]: https://img.shields.io/badge/-Blog-b45309?style=flat-square
[code-badge]: https://img.shields.io/badge/-Code-111827?style=flat-square&logo=github&logoColor=white
