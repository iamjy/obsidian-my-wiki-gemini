---
title: "CPU 아키텍처 (Core & Peripheral)"
date: 2026-05-21
tags: [cpu, core, peripheral, mcu, mpu, concept]
type: concept
status: active
source: "[[wiki/ingests/2026-05-21-embedded-platform-cpu]]"
related: ["[[wiki/concepts/embedded-platform]]", "[[wiki/concepts/risc-v]]"]
---

# CPU 아키텍처 (Core & Peripheral)

임베디드 시스템에서 CPU는 단순히 연산만 하는 장치가 아니라, 연산을 담당하는 **Core**와 주변장치를 제어하는 **Peripheral**의 결합체이다.

## 구성 요소

### 1. CPU Core
* **역할**: 산술 연산, 논리 연산, 데이터 처리 등 실제 계산을 수행.
* **성능 지표**: 비트 수(8/16/32/64 bit), 클럭 주파수, 아키텍처(ARM, [[wiki/concepts/risc-v|RISC-V]], x86 등).
* **보안 기능**: Arm 아키텍처의 경우 [[wiki/concepts/trustzone|Arm TrustZone]]과 같은 하드웨어 격리 기술을 통해 보안을 강화한다.
* 소프트웨어적 관점에서 OS의 구동 가능 여부를 결정하는 핵심 요소.

### 2. CPU Peripheral (주변장치 컨트롤러)
* **역할**: USB, Ethernet, UART, I2C, SPI 등 외부 장치와 Core 사이를 연결하고 제어.
* 하드웨어적 관점에서 별도의 외부 회로 없이 주변장치를 제어할 수 있게 하여 비용을 절감함.

## MPU vs MCU

| 구분 | MPU (Micro Processor Unit) | MCU (Micro Controller Unit) |
| --- | --- | --- |
| **중심** | CPU Core (연산 능력) | CPU Peripheral (제어 능력) |
| **특징** | 고성능 연산 중심, 외부 메모리 필요 | 저전력, 주변장치 컨트롤러 내장, One-chip 시스템 |
| **용도** | 스마트폰, 고성능 임베디드 리눅스 시스템 | 센서 제어, 가전제품, 단순 제어 시스템 |

## 임베디드 SW의 동작 원리
임베디드 소프트웨어는 프로그래밍 언어를 통해 CPU Peripheral 내의 **레지스터(Register)** 값을 조작함으로써 하드웨어의 동작을 제어한다. 즉, 하드웨어 제어의 본질은 레지스터 핸들링이다.
