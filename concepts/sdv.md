---
title: "SDV (Software Defined Vehicle)"
date: 2026-05-09
tags: [sdv, automotive, concept, software]
type: concept
status: active
source: "[[ingests/2026-05-09-sdv-verification-hils]]"
related: ["[[hils]]"]
---

# SDV (Software Defined Vehicle)

**SDV(Software Defined Vehicle, 소프트웨어 중심 자동차)**는 하드웨어가 아닌 소프트웨어가 차량의 주요 기능, 성능, 가치를 정의하는 자동차를 의미한다. 종종 '바퀴 달린 스마트폰'으로 비유된다.

## 핵심 특징
* **OTA(Over-The-Air) 업데이트**: 출고 이후에도 무선 네트워크를 통해 지속적으로 소프트웨어를 업데이트하여 새로운 기능을 추가하거나 주행 성능을 개선할 수 있다.
* **지속적 진화**: 기계공학적 스펙(마력, 서스펜션 등) 중심에서 벗어나, 차량의 생애 주기 내내 사용자 경험(UX)과 성능이 진화한다.
* **검증의 중요성 급증**: 수백만~수천만 줄의 코드가 수시로 업데이트되기 때문에, 새로운 코드가 주행 안전에 치명적인 영향을 미치지 않도록 검증하는 기술(예: [[hils]], CI/CD 파이프라인 자동화 등)이 개발의 핵심 경쟁력으로 대두되고 있다.
