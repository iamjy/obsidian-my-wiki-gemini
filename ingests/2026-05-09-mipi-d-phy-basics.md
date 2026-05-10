---
title: "MIPI 표준 및 D-PHY 기초"
date: 2026-05-09
tags: [mipi, hardware, interface, communication]
type: ingest
status: complete
source: "[[raw/Comprehensive Explanation MIPI is not difficult! Newbies learn the MIPI standard from scratch ~ Basics Part 1 What is D-PHY ~ - Semiconductor Business.md]]"
related: ["[[mipi]]", "[[mipi-d-phy]]"]
---

# MIPI 표준 및 D-PHY 기초

MIPI(Mobile Industry Processor Interface) 표준의 기본 개념과 물리 계층(Physical Layer) 중 하나인 D-PHY의 동작 원리 및 특징에 대한 영문 자료를 번역 및 요약한 내용.

## 1. MIPI 표준이란?
* **MIPI**: 2005년 MIPI Alliance에서 제정한 인터페이스 표준. 주로 스마트폰, 산업용 장비, 자동차 등의 카메라 및 디스플레이 장치에 널리 사용됨.
* **계층 구조**:
  * **물리 계층 (Physical Layer)**: D-PHY, M-PHY, C-PHY, A-PHY 등으로 나뉨.
  * **프로토콜 계층 (Protocol Layer)**: 용도에 따라 CSI-2(카메라 중심)와 DSI(디스플레이 중심) 등으로 나뉨.

## 2. D-PHY 및 DSI / CSI-2 차이점
* **기본 구성**: 1개의 클럭(Clock) 레인과 1, 2, 또는 4개의 데이터(Data) 레인으로 구성됨. 모두 차동 신호(Differential Signal)이며 클럭은 DDR 방식으로 동작.
* **DSI와 CSI-2의 D-PHY 차이**: 
  * 기본 구성은 동일하나, **DSI(Display Serial Interface)**의 경우 Data Lane 0이 양방향(Bi-directional) 통신을 지원하여 Slave 디바이스와 통신이 가능하다는 점이 다름.

## 3. D-PHY 전기적 특성 및 전송 모드
* D-PHY는 칩 내에서 두 가지 전송 모드를 동적으로 전환(Switching)하여 통신을 수행함.
  * **LP (Low Power) Mode**: 단일 종단(Single-ended) 출력, 1.2V 진폭, 최대 전송 속도 10Mbps. 저전력 제어에 사용.
  * **HS (High Speed) Mode**: 차동(Differential) 출력, ±200mV 진폭, 레인 당 최대 전송 속도 2.5Gbps. 고속 데이터 전송에 사용.

## 4. MIPI D-PHY와 LVDS 비교
* **전송 거리**: MIPI는 최대 30cm (단거리), LVDS는 최대 10m.
* **전송 속도**: 전송 거리가 짧은 대신 MIPI(D-PHY HS 모드 기준 최대 2.5Gbps)가 LVDS(최대 655Mbps)보다 훨씬 빠름.
* **동작 특징**: MIPI는 HS/LP 모드를 상황에 맞게 전환할 수 있어 고속 통신과 저전력을 동시에 구현함.
