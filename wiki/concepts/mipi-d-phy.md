---
title: "MIPI D-PHY"
date: 2026-05-09
tags: [mipi, hardware, physical-layer, concept]
type: concept
status: active
source: "[[wiki/ingests/2026-05-09-mipi-d-phy-basics]]"
related: ["[[wiki/concepts/mipi]]"]
---

# MIPI D-PHY

**D-PHY**는 [[wiki/concepts/mipi]] 인터페이스 표준의 가장 대표적인 물리 계층(Physical Layer) 규격 중 하나이다. 스마트폰이나 전장용 카메라/디스플레이와 AP 간의 데이터 전송에 주로 사용된다.

## 주요 특징 및 구조
* **레인(Lane) 구성**: 1개의 클럭 레인과 상황에 따라 1~4개의 데이터 레인으로 구성된다. 클럭은 DDR(Double Data Rate) 방식으로 동작한다.
* **프로토콜 호환성**: 카메라용인 CSI-2와 디스플레이용인 DSI 모두 D-PHY를 기반으로 동작할 수 있다. 
  * 단, DSI 환경에서는 Data Lane 0이 디스플레이 패널(Slave) 측의 정보를 읽어오기 위해 양방향(Bi-directional) 통신을 지원하는 차이가 있다.

## 전송 모드 (Transfer Modes)
D-PHY의 가장 큰 특징은 전력 소모를 최소화하기 위해 고속 모드와 저전력 모드를 동적으로 스위칭한다는 점이다.
* **HS (High Speed) Mode**:
  * 차동 신호(Differential) 방식 사용.
  * 진폭은 약 ±200mV (Common voltage 330mV)로 작음.
  * 초당 최대 2.5Gbps의 매우 빠른 속도로 데이터를 전송할 때 사용.
* **LP (Low Power) Mode**:
  * 단일 종단(Single-ended) 신호 방식 사용.
  * 진폭은 1.2V (Common voltage 0.6V).
  * 초당 최대 10Mbps로, 대기 상태나 제어 신호(Control)를 보낼 때 전력 소모를 최소화하기 위해 사용.

이러한 두 가지 모드의 동적 전환을 통해 짧은 거리(최대 30cm 내외)에서 초고속, 저전력 통신이 가능하다.
