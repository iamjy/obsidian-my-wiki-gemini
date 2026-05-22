---
title: "반도체 나오기 전부터 코드를 짜라…차량용 RISC-V 전환, 개발자가 먼저 준비할 것들"
date: 2026-05-14
tags: [infineon, risc-v, sdv, shift-left, virtual-prototype, mcu]
type: ingest
status: active
source: "https://www.e4ds.com/sub_view.asp?ch=5&t=0&idx=22408&c=1&ti=t"
related: ["[[wiki/concepts/sdv]]", "[[wiki/concepts/risc-v]]", "[[wiki/concepts/virtual-prototype]]", "[[wiki/concepts/embedded-development-process]]"]
---

# 차량용 RISC-V 전환과 시프트-레프트(Shift-Left) 개발 패러다임

## 핵심 요약
인피니언(Infineon)은 차세대 차량용 MCU에 오픈 표준 ISA인 **RISC-V**를 도입하며, SDV 시대의 짧아진 개발 주기에 대응하기 위해 하드웨어가 나오기 전 가상 환경에서 소프트웨어를 먼저 개발하는 **'시프트-레프트(Shift-Left)'** 전략을 강조함.

## 주요 내용

### 1. 인피니언의 RISC-V 도입 전략
* **멀티 아키텍처**: 기존 TriCore(AURIX), Arm(TRAVEO)과 함께 RISC-V를 병행하는 전략.
* **도입 배경**: SDV의 복잡한 요구(실시간 성능, 보안, 확장성, 이식성) 충족 및 차량 설계 복잡도 감소.
* **AURIX 포트폴리오 확장**: 차세대 AURIX 제품군에 RISC-V 코어 탑재 예정.

### 2. 시프트-레프트(Shift-Left)와 가상 프로토타입
* **개발 순서의 변화**: 실리콘(하드웨어)이 나오기 3~4년 전부터 가상 프로토타입(Virtual Prototype)을 통해 소프트웨어 개발 시작.
* **디지털 트윈(Digital Twin)**: 가상 프로토타입을 디지털 트윈으로 발전시켜, 하드웨어 출시 전 소프트웨어 컴포넌트 개발, 벤치마킹, 코드 프로파일링 완료.
* **이점**: 로우레벨 드라이버와 멀티코어 간 통신을 가상 환경에서 선행 확인하여 시장 출시 기간(Time-to-Market) 단축.

### 3. 개발자를 위한 준비 사항
* **프리-실리콘(Pre-Silicon) 개발 표준화**: 가상 환경에서의 부트, 기본 드라이버, 성능 프로파일링을 표준 프로세스로 편입.
* **툴체인 동등성(Toolchain Parity)**: 가상 환경과 실제 하드웨어 간의 컴파일러, 디버그, 트레이스 툴의 일관성 확보 및 검증.
* **SW 스택 성숙도 관리**: 칩 스펙뿐만 아니라 AUTOSAR, RTOS, 드라이버 포팅 준비 상태를 일정의 선행 조건으로 관리.
* **초기 보안/안전 설계**: 안전 라이브러리, 보안 컴포넌트, 통신 스택을 초기 단계부터 설계에 반영하고 산출물 체계 확인.

## 인사이트
* **'하드웨어를 기다리는 조직'에서 '가상 환경에서 먼저 완성도를 올리는 조직'으로의 체질 개선**이 SDV 시대의 핵심 경쟁력.
* RISC-V는 벤더 종속성을 낮추고, 모듈형 구조를 통해 자동차의 안전/보안 요구에 유연하게 대응할 수 있는 대안으로 부상.
* 2026년 3월 예정된 DRIVECORE 소프트웨어 번들에 RISC-V 가상 프로토타입 환경이 포함되는 등 툴체인 생태계가 구체화되고 있음.

## 연결된 개념
* [[wiki/concepts/sdv]]: 소프트웨어 중심 개발로의 전환과 검증의 중요성.
* [[wiki/concepts/risc-v]]: 오픈 표준 ISA의 도입 배경과 장점.
* [[wiki/concepts/virtual-prototype]]: 하드웨어 선행 개발을 위한 가상화 기술.
* [[wiki/concepts/embedded-development-process]]: 시프트-레프트 전략을 통한 전통적 프로세스의 변화.
