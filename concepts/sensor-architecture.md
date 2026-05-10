---
title: "센서 아키텍처 (Sensor Architecture)"
date: 2026-05-10
tags: [sensor, architecture, physical-ai, concept]
type: concept
status: active
source: "[[ingests/2026-05-10-physical-ai-sensor-start]]"
related: ["[[physical-ai]]", "[[perception]]"]
---

# 센서 아키텍처 (Sensor Architecture)

**센서 아키텍처**는 [[physical-ai]] 시스템(예: 휴머노이드 로봇, 자율주행차)에서 다수의 센서 데이터가 수집되어 AI 모델(인지) 및 액추에이터(제어)로 전달되기까지의 전체 흐름을 설계하는 방법론이다.

## 핵심 고려 사항
단순히 "어떤 센서를 몇 개 장착할 것인가"의 개별 스펙 문제를 넘어, 시스템 차원의 통합을 다룬다.
* **시간 동기화 (Time Synchronization)**: 서로 다른 주기로 데이터를 생성하는 여러 센서의 시간축을 일치시켜 왜곡 없는 인식을 보장한다.
* **공간 좌표계 통합**: 카메라, 라이다, IMU 등이 각각 인식하는 물리적 좌표계를 일치시킨다.
* **지연 시간 (Latency)**: 데이터 수집부터 제어 명령 하달까지의 지연을 최소화하여 실시간 반응성(엣지 컴퓨팅 연계)을 확보한다.
* **기능 안전 (Functional Safety)**: 센서 오작동 시 대응 메커니즘 설계 등 시스템의 신뢰성을 담보한다.

결과적으로 잘 설계된 센서 아키텍처는 **"센서 데이터가 제때, 올바른 형태로 제어 시스템에 도달하도록"** 보장하는 핵심 경쟁력이다.
