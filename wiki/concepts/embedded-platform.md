---
title: "임베디드 플랫폼"
date: 2026-05-21
tags: [embedded, platform, concept]
type: concept
status: active
source: "[[wiki/ingests/2026-05-21-embedded-platform-cpu]]"
related: ["[[wiki/concepts/cpu-architecture]]", "[[wiki/concepts/rtos]]", "[[wiki/concepts/embedded-development-process]]", "[[wiki/concepts/platform]]"]
---

# 임베디드 플랫폼 (Embedded Platform)

임베디드 시스템을 구성하는 기반 기술의 집합으로, 하드웨어, 소프트웨어, 그리고 개발 환경의 유기적인 결합을 의미한다. 넓은 의미의 [[wiki/concepts/platform|플랫폼]] 중 하드웨어/소프트웨어 제어에 특화된 형태이다.

## 구성 요소

1. **하드웨어 (Hardware)**
   * 핵심은 **CPU**이며, 시스템의 연산 능력과 주변장치 제어 능력을 결정한다.
   * 상세 구조: [[wiki/concepts/cpu-architecture]]

2. **소프트웨어 (Software)**
   * 시스템의 복잡도와 실시간성 요구사항에 따라 선택된다.
   * **Firmware**: 단순 반복 작업, 자원 공유 불필요, 우선순위 미적용 시 사용.
   * **[[wiki/concepts/rtos|RTOS]]**: 실시간 응답성과 우선순위 보장이 핵심인 경우 사용.
   * **Non-RTOS (General OS)**: 리눅스와 같이 고성능 연산과 복잡한 리소스 관리가 필요한 경우 사용.

3. **개발 환경 (Toolchain)**
   * 컴파일러, 디버거, IDE 등 소프트웨어를 개발하고 하드웨어에 배포하기 위한 도구들.

## 플랫폼 선정 기준
* **비용(Cost)**: 하드웨어 내장 컨트롤러 활용 여부, 라이선스 비용 등을 고려.
* **성능(Performance)**: CPU의 비트 수 및 클럭 속도가 OS 및 애플리케이션 요구사항을 만족하는지 확인.
* **개발 효율성**: 사용 가능한 라이브러리, 커뮤니티 지원, 툴체인의 편의성 등.
