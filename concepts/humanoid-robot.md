---
title: "휴머노이드 로봇 (Humanoid Robot)"
date: 2026-05-10
tags: [humanoid, robotics, physical-ai, concept]
type: concept
status: active
source: "[[ingests/2026-05-10-physical-ai-sensor-start]]"
related: ["[[physical-ai]]", "[[sensor-architecture]]"]
---

# 휴머노이드 로봇 (Humanoid Robot)

**휴머노이드 로봇**은 인간의 신체 구조와 유사한 형태를 지닌 로봇으로, 사람을 위해 설계된 비정형적인 환경에서 활동할 수 있도록 만들어진 [[physical-ai]]의 "통합 성적표"라 불린다.

## 기술적 특징
* **다중 감각의 융합**: 균형 유지, 물체 조작, 인간과의 상호작용 등을 수행하기 위해 시각 센서(RGB-D 카메라, 라이다 등)와 고유 수용성 감각 센서(IMU, Force-Torque 센서, 촉각 센서 등)를 결합하여 사용한다.
* **시스템 통합의 복잡성**: 두뇌(AI 모델), 감각(센서), 신경망(엣지 컴퓨팅), 행동(액추에이터 및 제어)이 고도로 유기적으로 결합되어야 하며, 이를 뒷받침하기 위해 [[sensor-architecture]] 설계가 필수적이다.
