---
title: "HILs (Hardware-in-the-Loop Simulation)"
date: 2026-05-09
tags: [hils, testing, simulation, automotive, concept]
type: concept
status: active
source: "[[ingests/2026-05-09-sdv-verification-hils]]"
related: ["[[sdv]]", "[[simulation]]"]
---

# HILs (Hardware-in-the-Loop Simulation)

**HILs(Hardware-in-the-Loop Simulation)**는 실제 자동차나 장비를 직접 구동하지 않고도, 실제와 같은 가상의 입출력 신호를 전자제어장치(ECU) 등 제어기에 주입하여 기기반응을 테스트하고 검증하는 기법 및 장비를 뜻한다.

## 기술적 한계와 진화
* **기존 HILs의 한계**: 주로 그래픽 기반의 가상 시뮬레이션 데이터를 주입하는 방식이었으나, 실제 도로의 미세한 노이즈나 변수를 완벽히 재현하기 어려워 실제 도로 테스트(실차 테스트)에서 미처 발견되지 못한 결함이 발생할 우려가 있었다.
* **실전형 HILs (Direct Injection)**: 최근의 HILs 환경은 가상 데이터 대신 실제 시험 차량이 주행하며 기록한 방대한 '로우 데이터(Raw Data)'를 제어기에 직접 주입(Direct Injection)하는 방식을 도입하고 있다. 이를 통해 제어기가 자신이 실제 도로 위에 있다고 착각할 만큼 현실과 동일한 100% 실전 환경의 신호를 바탕으로 검증 정확도를 획기적으로 높인다.

## 활용 (SDV 시대)
[[sdv]] 환경 하에서 CI/CD 파이프라인과 결합하여, 엔지니어 개입 없이 밤낮 24시간 자동으로 수만 가지 테스트 시나리오와 고장 주입(Fault Injection) 테스트를 수행함으로써 소프트웨어의 기능 안전성(ISO 26262) 및 사이버 보안(ISO 21434)을 효율적으로 확보하는 데 핵심 역할을 한다.
