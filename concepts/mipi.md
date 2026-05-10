---
title: "MIPI (Mobile Industry Processor Interface)"
date: 2026-05-09
tags: [mipi, interface, hardware, concept]
type: concept
status: active
source: "[[ingests/2026-05-09-mipi-d-phy-basics]]"
related: ["[[mipi-d-phy]]"]
---

# MIPI (Mobile Industry Processor Interface)

**MIPI**는 2005년 MIPI Alliance에서 모바일 기기(스마트폰 등) 및 연관 산업(자동차, 산업용 장비, IoT 등)을 위해 제정한 인터페이스 표준 규격이다. 

## 주요 목적 및 적용 분야
* 주로 디바이스 내부의 **카메라 모듈**과 **디스플레이 모듈**을 애플리케이션 프로세서(AP)와 연결하기 위해 고안되었다.
* 모바일 환경의 특성에 맞게 **고속 데이터 전송**과 **저전력 소모**를 동시에 달성하는 것을 핵심 목표로 한다.

## 계층 구조
MIPI 표준은 크게 물리적 신호 전송을 담당하는 **Physical Layer**와 데이터 패킷 및 통신 규약을 정의하는 **Protocol Layer**로 나뉜다.
* **Physical Layer**: D-PHY, M-PHY, C-PHY, A-PHY 등. (참고: [[mipi-d-phy]])
* **Protocol Layer**: 
  * **CSI-2 (Camera Serial Interface 2)**: 카메라 모듈용 프로토콜.
  * **DSI (Display Serial Interface)**: 디스플레이 모듈용 프로토콜.
