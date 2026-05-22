---
title: "A²B (Automotive Audio Bus)"
date: 2026-05-11
tags: [automotive, audio, networking, hardware]
type: concept
status: active
source: "https://www.analog.com/en/applications/technology/a2b-audio-bus.html"
related: ["[[wiki/concepts/sdv]]", "[[wiki/concepts/sensor-architecture]]"]
---

# A²B (Automotive Audio Bus)

**A²B (Automotive Audio Bus)**는 아나로그디바이스(ADI)에서 개발한 고성능 디지털 오디오 버스 기술이다. 차량 내 오디오, 센서, 제어 신호를 단일 트위스티드 페어 케이블을 통해 저지연(Low Latency)으로 전송하기 위해 설계되었다.

## 주요 특징
- **확정적 저지연(Deterministic Low Latency)**: 신호 전송 지연 시간이 매우 짧고 일정하여 실시간 제어 및 오디오 동기화에 최적화됨. (A²B 2.0 기준 약 62μs)
- **배선 단순화**: 무거운 아날로그 배선을 단일 비차폐 트위스티드 페어(UTP) 케이블로 대체하여 차량 중량을 줄이고 복잡도를 낮춤.
- **전력 및 데이터 동시 전송**: 동일한 케이블을 통해 데이터와 전력을 동시에 공급 가능.
- **데이지 체인(Daisy Chain) 구조**: 여러 노드를 직렬로 연결하여 시스템 확장성이 뛰어남.

## A²B 2.0의 진화
A²B 2.0은 [[wiki/concepts/sdv]] 환경에 맞춰 다음과 같은 기능이 강화되었다:
- **이더넷 터널링(Ethernet Tunneling)**: OASPI 표준을 통해 차량용 이더넷 아키텍처와 통합 가능. 오디오 전 전용망이 아닌 전체 차량 네트워크의 일부로 동작.
- **대역폭 확대**: 양방향 최대 98.3Mbps 제공 (이전 세대 대비 4배).
- **채널 수 증가**: 업스트림/다운스트림 각각 최대 119개의 오디오 채널 지원.
- **비용 효율성**: 외부 부품 수 절감 및 기존 A²B 1.0 하드웨어와의 호환성 유지.

## 주요 활용 분야
- **프리미엄 오디오 시스템**: 다채널 사운드 구현.
- **RNC (Road Noise Cancellation)**: 노면 소음 제거 기술.
- **PSZ (Personal Sound Zone)**: 좌석별 개별 오디오 존 구축.
- **안전 기능**: 긴급 통화(E-Call), 보행자 경고음 시스템 등.
