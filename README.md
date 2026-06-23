<div align="center">

<h1>Awesome Agent-for-Infra</h1>

[![Awesome][awesome-badge]](https://github.com/sindresorhus/awesome)
[![Repository][repo-badge]](https://github.com/haodongwang01/Awesome-Agent-for-Infra)
[![License][license-badge]](LICENSE)

</div>

> We welcome issues and pull requests for missing papers, toolchains, benchmarks, and reproducible agent workflows around AI infrastructure.

## 🎉 News

- **[2026 Jun 18]** Released the initial four-track map for AI agents in infrastructure.

## 📖 Contents

- [🎉 News](#-news)
- [📖 Contents](#-contents)
- [🧭 Survey Map](#-survey-map)
  - [Hardware and Architecture Design](docs/hardware-architecture.md)
    - [Paper](docs/hardware-architecture.md#paper)
      - [Papers and Benchmarks](docs/hardware-architecture.md#papers-and-benchmarks)
    - [Skills](docs/hardware-architecture.md#skills)
    - [Toolchain](docs/hardware-architecture.md#toolchain)
  - [Operators, Kernels and Compilers](docs/operators-kernels-compilers.md)
    - [Paper](docs/operators-kernels-compilers.md#paper)
      - [Benchmarks and Evaluation](docs/operators-kernels-compilers.md#benchmarks-and-evaluation)
      - [Trained Kernel-Generation Agents](docs/operators-kernels-compilers.md#trained-kernel-generation-agents)
      - [Agentic Kernel Optimization Frameworks](docs/operators-kernels-compilers.md#agentic-kernel-optimization-frameworks)
      - [LLM-Agent Algorithm-Discovery Precedents](docs/operators-kernels-compilers.md#llm-agent-algorithm-discovery-precedents)
    - [Skills](docs/operators-kernels-compilers.md#skills)
    - [Toolchain](docs/operators-kernels-compilers.md#toolchain)
  - [Model Serving and System Optimization](docs/model-serving-system-optimization.md)
    - [Paper](docs/model-serving-system-optimization.md#paper)
      - [Serving Systems and Papers](docs/model-serving-system-optimization.md#serving-systems-and-papers)
    - [Skills](docs/model-serving-system-optimization.md#skills)
    - [Toolchain](docs/model-serving-system-optimization.md#toolchain)
  - [Environments and Benchmarks](docs/environments-benchmarks.md)
    - [Paper](docs/environments-benchmarks.md#paper)
      - [Benchmarks](docs/environments-benchmarks.md#benchmarks)
    - [Skills](docs/environments-benchmarks.md#skills)
    - [Toolchain](docs/environments-benchmarks.md#toolchain)
- [🌟 Acknowledgment](#-acknowledgment)

## 🧭 Survey Map

| Track | Core Problem | Details |
|:-:|:-|:-:|
| Hardware and Architecture Design | Can agents turn design intent into verified and optimized hardware artifacts under simulator, synthesis, and PPA feedback? | [![Open][open-badge]](docs/hardware-architecture.md) |
| Operators, Kernels and Compilers | Can agents generate, repair, and optimize kernels or compiler transformations using compile errors, tests, profiler traces, and hardware feedback? | [![Open][open-badge]](docs/operators-kernels-compilers.md) |
| Model Serving and System Optimization | Can agents tune serving engines, schedulers, deployments, and runtime configs to satisfy latency, throughput, reliability, and cost goals? | [![Open][open-badge]](docs/model-serving-system-optimization.md) |
| Environments and Benchmarks | How should infra agents be evaluated with executable tasks, stable harnesses, reproducible metrics, and auditable baselines? | [![Open][open-badge]](docs/environments-benchmarks.md) |

## 🌟 Acknowledgment

This survey is built from the open papers, benchmarks, and systems maintained by the AI infrastructure community. The README structure draws inspiration from [TsinghuaC3I/Awesome-RL-for-LRMs](https://github.com/TsinghuaC3I/Awesome-RL-for-LRMs).

[awesome-badge]: https://img.shields.io/badge/Awesome-List-0f766e?style=flat-square&logo=awesome-lists&logoColor=white
[repo-badge]: https://img.shields.io/badge/Repo-Awesome--Agent--for--Infra-334155?style=flat-square&logo=github&logoColor=white
[license-badge]: https://img.shields.io/badge/License-MIT-64748b?style=flat-square
[open-badge]: https://img.shields.io/badge/-Open-475569?style=flat-square
