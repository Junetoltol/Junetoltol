# Hi, I'm Junetoltol 👋

Information & Communication Engineering student focused on **Edge AI, on-device inference, and Physical AI systems**.

I am interested in a practical systems question: **how can AI models run efficiently and reliably under real device constraints?** I explore that question through embedded devices, controlled measurement, and kernel-level profiling.

## Research interests

- **Edge / On-device AI** — model quantization, GPU offload, memory use, latency, and throughput
- **Physical AI** — the interaction between perception, compute resources, and real-world action
- **AI systems profiling** — separating end-to-end behavior from individual kernel behavior
- **IoT systems** — sensing and control with Raspberry Pi and embedded peripherals

## Current projects

### LG Aimers Hackathon — In progress

I am currently working on an LG Aimers hackathon project. The repository will be published once the implementation and results are ready to share.

### Secure Dynamic Edge AI — Planned for Fall 2026

This team project will explore multi-sensor verification and quantization robustness on Raspberry Pi. The repository will remain private during development.

## Completed experiments

### LLM inference on Jetson Orin Nano — Completed

I profiled Qwen3.5-2B inference with `llama.cpp`, NVIDIA Nsight Systems, and Nsight Compute.

| Comparison | Observed result |
|---|---|
| Whole-prefill throughput, B=384 → B=512 | `916.24 ± 32.67` → `992.18 ± 38.02 token/s` (**+8.3%**) |
| Selected BF16 Tensor Core GEMM kernel | `9.636 ± 0.538` → `8.564 ± 0.230 TFLOP/s` (**−11.1%**) |

**Takeaway:** a slower sampled kernel does not necessarily mean lower whole-model throughput. I report kernel-level and end-to-end measurements separately and control workload, warm-up, clocks, and repetitions.

📌 [Edge AI profiling repository](https://github.com/Junetoltol/edge-ai-jetson-mini-project)

### Offline meeting transcription on Jetson Orin Nano — Completed

Built and evaluated an offline Korean meeting-transcription pipeline combining speech recognition, local LLM correction, and speech synthesis on a resource-constrained edge device.

📌 [Meeting transcription repository](https://github.com/Junetoltol/jetson-meeting-transcription-poc)

## Selected projects

| Project | What it shows | Stack |
|---|---|---|
| [Edge AI on Jetson](https://github.com/Junetoltol/edge-ai-jetson-mini-project) | Completed Jetson Orin Nano inference experiments with end-to-end and kernel-level profiling | Jetson, `llama.cpp`, Nsight Systems / Compute |
| [Offline Meeting Transcription](https://github.com/Junetoltol/jetson-meeting-transcription-poc) | Completed edge pipeline for Korean speech recognition, local LLM correction, and speech synthesis | Jetson, Whisper, local LLM, TTS |
| [IoT Systems coursework](https://github.com/Junetoltol/Assignments/tree/main/IotSystem-main) | Raspberry Pi sensing and control with PIR, DHT11, ultrasonic, gas, light, soil-moisture, motors, and simple vision exercises | C, Python, Raspberry Pi, OpenCV |
| [Job Buddy](https://github.com/Junetoltol/WebProject2025ICE) | Team repository for an AI-assisted resume and cover-letter web service | FastAPI, OpenAI / Gemini APIs, Spring Boot, React, MySQL |

## Tools I work with

- **Languages:** Python, C/C++, Java, Kotlin
- **Edge & AI systems:** Jetson Orin Nano, Raspberry Pi, `llama.cpp`, CUDA, model quantization
- **Profiling:** NVIDIA Nsight Systems, Nsight Compute, controlled benchmarking
- **Application development:** FastAPI, Spring Boot, React, MySQL, Android / Jetpack Compose

## Teaching and learning

- Supporting hands-on learning as an **IoT Systems teaching assistant**
- Currently studying **Physical AI / Cyber-Physical AI**, efficient LLM inference, and experimental methodology for AI systems
- Turning course experiments into reproducible repositories with clear setup, measurements, and limitations

## How I approach experiments

`Question → controlled setup → end-to-end measurement → kernel inspection → interpretation → limitations`

I prefer evidence-backed conclusions and explicitly separate what was measured from what is inferred.
