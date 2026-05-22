---
title: "NPU (Neural Processing Unit)"
date: 2026-05-14
tags: [npu, ai-semiconductor, hardware, concept]
type: concept
status: active
source: "[[wiki/ingests/2026-05-14-mobilint-edge-ai-inference]]"
related: ["[[wiki/concepts/on-device-ai]]", "[[wiki/concepts/edge-ai]]", "[[wiki/concepts/inference]]"]
---

# NPU (신경망 처리 장치)

**NPU(Neural Processing Unit)**는 딥러닝 아키텍처의 핵심인 대규모 행렬 연산을 효율적으로 처리하기 위해 설계된 인공지능 전용 가속기이다. GPU에 비해 AI 연산에 특화되어 전력 효율(전성비)과 성능이 뛰어나다.

## 핵심 설계 쟁점
NPU 설계는 크게 **범용성(Programmability)**과 **효율성(Efficiency)** 사이의 균형을 맞추는 것이 핵심이다.

* **저정밀 연산**: 딥러닝 모델은 높은 정밀도가 필요하지 않은 경우가 많아, FP32 대신 INT8, INT4 등 저정밀 데이터 타입을 사용하여 연산 속도를 높이고 메모리 대역폭을 절약한다.
* **메모리 계층 구조 최적화**: 데이터 이동을 최소화하기 위해 스크래치패드 메모리(Scratchpad Memory)나 멀티레벨 메모리 구조를 활용하여 데이터 접근 패턴을 최적화한다.
* **실성능(Utilization)**: 단순히 이론적인 최대 성능(TOPS, Tera Operations Per Second)보다, 실제 모델을 구동했을 때 하드웨어 자원이 얼마나 효율적으로 사용되는지가 중요하다.

## 풀스택 최적화 (Full-stack Optimization)
NPU의 경쟁력은 하드웨어 자체뿐만 아니라 이를 뒷받침하는 소프트웨어 생태계에서 나온다.
* **컴파일러**: 고수준 AI 프레임워크(PyTorch, TensorFlow 등)로 작성된 모델을 NPU 아키텍처에 맞게 최적화하여 컴파일하는 기술.
* **알고리즘 연동**: 최신 트랜스포머(Transformer) 계열 모델(LLM, VLM) 지원 및 모델 경량화 기법과의 시너지.

## 주요 형태
1. **가속기 (Accelerator)**: 호스트 CPU에 연결되어 AI 연산만을 보조하는 역할 (예: 모빌린트 에리스).
2. **AI SoC (System on Chip)**: NPU뿐만 아니라 CPU, ISP, DSP, 통신 인터페이스 등을 하나의 칩에 통합하여 독립적으로 구동 가능 (예: 모빌린트 레귤러스).
