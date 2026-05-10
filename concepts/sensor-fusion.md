---
title: "센서 퓨전 (Sensor Fusion)"
date: 2026-05-10
tags: [sensor, sensor-fusion, perception, physical-ai, concept]
type: concept
status: active
source: "[[ingests/2026-05-10-physical-ai-sensor-edge]]"
related: ["[[perception]]", "[[physical-ai]]", "[[sensor-architecture]]"]
---

# 센서 퓨전 (Sensor Fusion)

**센서 퓨전(Sensor Fusion)**은 서로 다른 물리적 원리나 특징을 가진 여러 개의 센서 데이터를 결합하여 단일 센서의 한계를 극복하고 대상이나 환경에 대해 더 정확하고 신뢰성 있는 인식을 도출하는 기술이다.

## 도입 배경 및 필요성
* **단일 센서의 한계 극복**: 카메라 센서는 빛(역광, 어둠)이나 날씨(비, 안개)에 취약하며, 단독으로는 오판(False Positive)을 내릴 확률이 존재한다.
* **상호 보완적 특징 활용**: 카메라(고해상도 색상, 형태 인식), 라이다(LiDAR, 정밀한 거리 및 3D 형상), 레이더(Radar, 날씨 영향 적음, 속도 감지), IMU(관성 측정) 등을 결합하여 각 센서의 약점을 보완한다.
* **안전성 강화**: [[physical-ai]](자율주행, 휴머노이드 등)가 불규칙한 실제 환경에서 구동될 때 충돌 방지와 즉각적인 판단을 위한 필수 기반 기술이 된다.
