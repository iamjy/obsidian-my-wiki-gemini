---
title: "임베디드 플랫폼과 CPU의 이해"
date: 2026-05-21
tags: [embedded, cpu, mcu, mpu, rtos, ingest]
type: ingest
status: active
source: "https://devsophia.tistory.com/entry/01-%EC%9E%84%EB%B2%A0%EB%94%94%EB%93%9C-%ED%94%8C%EB%9E%AB%ED%8F%BC-CPU"
related: ["[[wiki/concepts/embedded-platform]]", "[[wiki/concepts/cpu-architecture]]", "[[wiki/concepts/rtos]]"]
---

# 임베디드 플랫폼과 CPU의 이해

## 개요
임베디드 시스템의 기초가 되는 플랫폼의 구성 요소와 CPU의 내부 구조(Core 및 Peripheral), 그리고 MPU와 MCU의 차이점에 대해 기술함.

## 주요 내용

### 1. 임베디드 플랫폼의 구성
* **구성**: 하드웨어(CPU) + 소프트웨어(Firmware 또는 OS) + 개발환경(Tool).
* **소프트웨어 선택 기준**:
    * **Firmware**: Task 수가 적고 자원 공유가 없으며 우선순위가 필요 없는 경우.
    * **RTOS**: Task 수는 적지만 실시간 우선순위 보장이 필요한 경우.
    * **Non-RTOS**: 여러 Task가 동일 자원에 접근해야 하는 복잡한 시스템.

### 2. CPU의 구조
* **CPU = CPU Core + CPU Peripherals (주변장치 컨트롤러)**.
* **CPU Peripheral**: USB, Ethernet MAC 등 주변장치와 Core 사이를 연결하여 하드웨어를 제어하는 역할.
* **하드웨어 관점**: 필요한 컨트롤러가 내장된 CPU를 선정하여 비용 절감.
* **소프트웨어 관점**: CPU의 비트 수(연산 능력)에 따라 OS 지원 여부 결정 (예: 리눅스는 32bit 이상 필요).

### 3. MPU vs MCU
* **MPU (Micro Processor Unit)**: CPU Core의 연산 처리 능력이 중심인 프로세서.
* **MCU (Micro Controller Unit)**: CPU Peripheral이 중심이 되어 주변장치 제어 회로가 내부에 통합된 프로세서.

### 4. 임베디드 소프트웨어의 본질
* 프로그래밍 언어(C 등)를 사용하여 주변장치의 **레지스터(Register)** 값을 설정함으로써 하드웨어를 제어하는 실행 코드.

## 핵심 요약
* 임베디드 플랫폼은 비용 효율성을 고려하여 HW, SW, Tool을 적절히 조합해야 함.
* CPU 선정 시 하드웨어적(Peripheral) 요구사항과 소프트웨어적(Core) 요구사항을 모두 고려해야 함.
* 임베디드 개발의 핵심은 레지스터 제어를 통한 하드웨어 핸들링임.
