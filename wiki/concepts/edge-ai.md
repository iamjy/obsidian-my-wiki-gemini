---
title: "엣지 AI (Edge AI)"
date: 2026-05-10
tags: [edge-ai, physical-ai, computing, concept]
type: concept
status: active
source: "[[wiki/ingests/2026-05-10-physical-ai-sensor-edge]]"
related: ["[[wiki/concepts/on-device-ai]]", "[[wiki/concepts/physical-ai]]", "[[wiki/concepts/sensor-architecture]]"]
---

# 엣지 AI (Edge AI)

**엣지 AI(Edge AI)**는 중앙 클라우드 서버 대신, 데이터가 발생하고 소비되는 물리적 위치(디바이스 자체나 디바이스와 가까운 로컬 네트워크)에서 즉각적으로 인공지능 연산 및 추론을 수행하는 기술 방식이다. 

## 필요성과 역할
* **지연 시간(Latency) 최소화**: 클라우드 왕복 통신으로 인해 발생하는 지연을 없애준다. 특히 휴머노이드 로봇이나 자율주행과 같은 [[wiki/concepts/physical-ai]]에서는 지연 시간이 곧 치명적인 안전 문제로 직결되므로 실시간 반응성을 확보하기 위해 엣지 AI가 필수적이다.
* **추론(Inference) 시장의 급성장**: 생성형 AI와 에이전트 AI의 확산으로, 학습보다 학습된 모델을 현장에서 실행하는 추론 수요가 엣지로 빠르게 이동하고 있다.
* **지능형 엣지 센서 및 NPU**: 센서 자체나 모듈 내에 신호 처리, 통신, 추론 기능을 결합하여 유의미한 정보만을 선별해 제어 단으로 넘기는 분산 아키텍처 형태로 진화하고 있다. 이를 위해 [[wiki/concepts/npu]]와 같은 저전력/고성능 추론 가속기의 역할이 핵심적이다.
* **독립성과 프라이버시**: 외부 네트워크 연결이 끊긴 오프라인 상태에서도 동작이 가능하며, 민감한 원시 데이터(비전, 음성 등)가 클라우드로 전송되지 않아 보안이 강화된다.

휴머노이드의 인지-판단-제어 루프는 점차 **'센서(퓨전) → 엣지 추론 → 즉시 제어'**의 형태로 자리잡고 있다. 엣지 환경에서는 이론적인 TOPS 성능보다 실제 모델 구동 시의 하드웨어 유틸라이제이션(Utilization)과 소프트웨어 풀스택 최적화가 실질적인 가치를 결정한다.
