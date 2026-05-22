---
title: "TEE (Trusted Execution Environment)"
date: 2026-05-22
tags: [security, architecture, concept]
type: concept
status: active
source: "[[wiki/ingests/2026-05-22-op-tee-basics]]"
related: ["[[wiki/concepts/trustzone]]", "[[wiki/concepts/op-tee]]"]
---

# TEE (Trusted Execution Environment)

**TEE(신뢰 실행 환경)**는 메인 프로세서 내의 보안 영역으로, 이곳에 저장된 코드와 데이터가 기밀성(Confidentiality)과 무결성(Integrity)을 보호받도록 보장한다.

## 주요 개념
* **격리(Isolation)**: 일반 운영체제(Rich OS, 예: 리눅스, 안드로이드)가 구동되는 영역(REE)으로부터 하드웨어적으로 완전히 격리된 실행 환경을 제공한다.
* **보안 애플리케이션(Trusted Application, TA)**: TEE 내에서만 실행되는 특수 애플리케이션으로, 암호화 키 관리, 결제 처리, 생체 인식 정보 처리 등 보안이 중요한 로직을 담당한다.

## 특징
* **보안성**: REE의 커널이 탈취되더라도 TEE 내부의 자원에는 접근할 수 없도록 설계된다.
* **성능**: 보안 소자(Secure Element, SE)와 달리 메인 프로세서의 자원을 활용하므로 상대적으로 빠른 연산 처리가 가능하다.

## 주요 구현체
* **[[wiki/concepts/op-tee|OP-TEE]]**: 오픈 소스 기반 TEE.
* **Qualcomm QSEE / Trusty (Google)**: 안드로이드 기기에서 주로 사용되는 TEE.
* **Intel SGX**: x86 아키텍처용 신뢰 실행 환경.
