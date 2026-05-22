---
title: "Arm TrustZone"
date: 2026-05-22
tags: [arm, architecture, security, hardware, concept]
type: concept
status: active
source: "[[wiki/ingests/2026-05-22-op-tee-basics]]"
related: ["[[wiki/concepts/tee]]", "[[wiki/concepts/cpu-architecture]]"]
---

# Arm TrustZone

**Arm TrustZone**은 단일 CPU 코어를 두 개의 가상 영역인 **보안 세계(Secure World)**와 **비보안 세계(Normal World/Non-secure World)**로 나누어 관리하는 하드웨어 보안 기술이다.

## 핵심 메커니즘
* **NS bit (Non-Secure bit)**: 시스템 버스(AMBA AXI)를 통해 전달되는 신호에 보안 상태를 나타내는 비트를 추가하여, 하드웨어 레벨에서 접근 제어를 수행한다.
* **보안 모니터 (Secure Monitor)**: 두 세계 간의 전환을 관리하는 특수 모드(SMC 명령어 사용).
* **자원 격리**: 메모리(TZASC), 주변장치(TZPC), 인터럽트 등을 특정 세계에서만 접근 가능하도록 설정할 수 있다.

## 특징
* **보안 아키텍처의 근간**: 모바일 및 임베디드 기기에서 [[wiki/concepts/tee|TEE]]를 구현하기 위한 핵심 하드웨어 기반을 제공한다.
* **효율성**: 별도의 보안 프로세서를 추가하지 않고도 메인 CPU의 자원을 안전하게 공유하여 비용을 절감할 수 있다.

## 적용 범위
* Arm Cortex-A, Cortex-M(v8-M 이후) 시리즈 등 대부분의 현대적 Arm 아키텍처에 포함되어 있다.
