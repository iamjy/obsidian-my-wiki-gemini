---
title: "RTOS (Real-Time Operating System)"
date: 2026-05-21
tags: [embedded, os, rtos, concept]
type: concept
status: active
source: "[[wiki/ingests/2026-05-21-embedded-platform-cpu]]"
related: ["[[wiki/concepts/embedded-platform]]"]
---

# RTOS (Real-Time Operating System)

실시간 응답성을 보장하기 위해 설계된 운영체제. 일반적인 OS(Non-RTOS)가 처리량(Throughput)을 최적화하는 반면, RTOS는 결정론적(Deterministic) 수행 시간과 우선순위 보장을 최우선으로 한다.

## 선정 기준
임베디드 시스템에서 소프트웨어를 선택할 때 RTOS는 다음과 같은 조건에서 고려된다:
* **우선순위 보장**: Task의 수가 적더라도 특정 작업의 수행 시간이 엄격하게 지켜져야 하는 경우.
* **실시간성(Real-time)**: 외부 이벤트에 대해 정해진 데드라인 내에 반응해야 하는 시스템 (예: 에어백 제어, 드론 비행 제어).

## 특징
* **선점형 멀티태스킹 (Preemptive Multitasking)**: 높은 우선순위의 Task가 언제든 CPU를 점유할 수 있음.
* **낮은 지연 시간 (Low Latency)**: 인터럽트 발생 시 즉각적인 처리를 지원.
* **결정론적 동작**: 동일한 입력에 대해 항상 일정한 시간 내에 결과를 출력함.
