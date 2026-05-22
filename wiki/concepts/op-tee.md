---
title: "OP-TEE (Open Portable TEE)"
date: 2026-05-22
tags: [security, arm, op-tee, open-source, concept]
type: concept
status: active
source: "[[wiki/ingests/2026-05-22-op-tee-basics]]"
related: ["[[wiki/concepts/tee]]", "[[wiki/concepts/trustzone]]"]
---

# OP-TEE (Open Portable TEE)

**OP-TEE**는 [[wiki/concepts/trustzone|Arm TrustZone]] 기술을 사용하여 구현된 오픈 소스 [[wiki/concepts/tee|신뢰 실행 환경(TEE)]]이다. Trusted Firmware 프로젝트의 일부로 관리되며, 임베디드 리눅스 시스템을 위한 표준적인 보안 솔루션으로 자리 잡고 있다.

## 주요 구성 요소
1. **OP-TEE OS**: 보안 세계(Secure World)에서 실행되는 커널 수준의 보안 운영체제.
2. **TEE Client API (libteec)**: 비보안 세계(Normal World)의 애플리케이션이 TEE와 통신하기 위해 사용하는 라이브러리.
3. **TEE Internal Core API**: 보안 애플리케이션(TA)이 OP-TEE OS의 기능을 사용하기 위해 호출하는 API.
4. **OP-TEE Linux Kernel Driver**: 리눅스 커널과 OP-TEE OS 사이의 통신 브리지 역할을 수행.

## 주요 장점
* **오픈 소스**: 소스 코드가 공개되어 있어 투명한 보안 검증이 가능하며 커스터마이징이 용이하다.
* **표준 준수**: GlobalPlatform 규격을 준수하여 높은 호환성을 제공한다.
* **이식성 (Portability)**: 다양한 Arm SoC(NXP, ST, TI, Xilinx 등)에 포팅되어 있다.

## 활용 사례
* 암호화 키 관리 및 하드웨어 암호 가속기 제어.
* 안전한 부팅(Secure Boot) 프로세스 지원.
* DRM(Digital Rights Management) 콘텐츠 보호.
* 지문 인식, 얼굴 인식 등 생체 인식 정보 보호.
