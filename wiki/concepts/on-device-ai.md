---
title: "On-device AI"
date: 2026-05-09
tags: [concept, edge-computing, optimization]
type: concept
status: active
source: ""
related: ["[[wiki/concepts/physical-ai]]", "[[wiki/ingests/2026-05-09-physical-ai-simulation-on-device]]"]
---

# On-device AI (온디바이스 AI)

## 정의
중앙 서버나 클라우드를 거치지 않고, 기기(스마트폰, 로봇, 웨어러블 등) 내부에서 직접 AI 연산을 수행하는 기술.

## 장점
- **저지연(Low Latency)**: 네트워크 통신 단계를 생략하여 실시간 반응 가능.
- **보안성**: 민감한 데이터를 기기 외부로 전송하지 않음.
- **안정성**: 네트워크 연결이 불안정한 환경에서도 동작 보장.

## 핵심 기술
- **모델 경량화**: 양자화(Quantization), 가지치기(Pruning) 등.
- **NPU 최적화**: 신경망 연산 전용 하드웨어인 [[wiki/concepts/npu|NPU]] 활용.
