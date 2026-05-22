---
title: "추론 (Inference)"
date: 2026-05-14
tags: [inference, deep-learning, concept]
type: concept
status: active
source: "[[wiki/ingests/2026-05-14-mobilint-edge-ai-inference]]"
related: ["[[wiki/concepts/npu]]", "[[wiki/concepts/edge-ai]]", "[[wiki/concepts/on-device-ai]]"]
---

# 추론 (Inference)

**추론(Inference)**은 이미 학습이 완료된 AI 모델에 새로운 데이터를 입력하여 결과를 도출해내는 과정을 말한다. AI의 생애 주기에서 '학습(Training)'이 지식을 습득하는 과정이라면, '추론'은 습득한 지식을 실제 서비스나 제품에서 사용하는 단계이다.

## 시장의 변화: 학습에서 추론으로
과거 AI 시장은 데이터센터를 중심으로 한 대규모 모델 학습 경쟁이 주를 이루었으나, 점차 학습된 모델을 실제 현장에 적용하여 가치를 창출하는 추론 시장의 비중이 커지고 있다.

* **수요 급증**: '에이전트 AI'의 확산과 다양한 온디바이스 AI 기기의 등장으로 실시간 추론 수요가 폭증함.
* **엣지 이동**: 클라우드 서버뿐만 아니라, 데이터가 발생하는 현장(엣지)에서 즉각적인 추론을 수행하려는 경향이 강해짐.

## 추론 최적화의 중요성
추론 단계에서는 학습과 달리 **실시간성(Low Latency)**과 **비용 효율성**이 가장 중요하다.
* **가성비 및 전성비**: 동일한 비용과 전력으로 얼마나 많은 추론 세션을 처리할 수 있는지가 핵심 경쟁력이다.
* **모델 경량화**: 엣지 기기의 제한된 자원에서 동작하기 위해 양자화(Quantization), 가지치기(Pruning) 등을 통해 모델 크기를 줄여 추론 속도를 높인다.

## 관련 기술
* [[wiki/concepts/npu]]: 추론 연산에 최적화된 하드웨어.
* [[wiki/concepts/edge-ai]]: 현장에서의 즉각적인 추론 수행.
