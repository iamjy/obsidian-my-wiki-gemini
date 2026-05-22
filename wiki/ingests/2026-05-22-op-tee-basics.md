---
title: "OP-TEE"
date: 2026-05-22
tags: [security, tee, trustzone, arm, op-tee, ingest]
type: ingest
status: active
source: "https://www.trustedfirmware.org/projects/op-tee/"
related: ["[[wiki/concepts/tee]]", "[[wiki/concepts/trustzone]]", "[[wiki/concepts/op-tee]]"]
---

# OP-TEE 개요

## 개요
OP-TEE(Open Portable Trusted Execution Environment)는 Arm TrustZone 기술을 사용하는 Arm A-Profile 시스템(Armv8-A, Armv7-A)에서 비보안 리눅스 커널과 함께 동작하도록 설계된 신뢰 실행 환경(TEE)이다.

## 주요 특징
* **타겟 아키텍처**: Arm Cortex-A 코어 기반 시스템.
* **보안 기술**: Arm TrustZone 하드웨어 보안 기술 활용.
* **표준 준수**: GlobalPlatform API 사양을 구현함.
    * **TEE Internal Core API v1.1.x**: 신뢰 애플리케이션(Trusted Application, TA)에 노출되는 API.
    * **TEE Client API v1.0**: TEE와 통신하는 방법을 정의하는 클라이언트 측 API.

## 구성 요소 간 상호작용
* **REE (Rich Execution Environment)**: 일반적인 리눅스 커널이 구동되는 환경.
* **TEE (Trusted Execution Environment)**: OP-TEE OS와 TA가 구동되는 보안 환경.
* REE의 클라이언트 애플리케이션은 TEE Client API를 통해 TEE 내의 TA에 서비스를 요청하며, 보안이 중요한 연산은 TEE 내에서 격리되어 처리된다.

## 시사점
OP-TEE는 오픈 소스 기반의 신뢰할 수 있는 펌웨어(Trusted Firmware) 프로젝트의 일부로, 모바일 기기 및 임베디드 시스템의 보안 강화(결제, DRM, 키 관리 등)를 위한 핵심 인프라로 널리 사용된다.
