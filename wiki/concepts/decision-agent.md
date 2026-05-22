---
title: "의사결정 AI 에이전트 (Decision AI Agent)"
date: 2026-05-10
tags: [ai-agent, decision-making, kpi, concept]
type: concept
status: active
source: "[[wiki/ingests/2026-05-10-ai-agent-kpi-decision]]"
related: ["[[wiki/concepts/semantic-layer]]"]
---

# 의사결정 AI 에이전트 (Decision AI Agent)

**의사결정 AI 에이전트**는 단순한 질의응답이나 문서 요약을 넘어서, 기업의 핵심 성과 지표(KPI)를 분석하고 실질적인 비즈니스 개선 방안을 제안하는 데이터 분석 중심의 자율적 인공지능 에이전트이다. 최근에는 생성형 AI를 넘어 스스로 판단하고 행동하는 **에이전트 AI (Agent AI)**로 진화하며, 대규모 학습 시장을 넘어 실제 현장에서의 실시간 [[wiki/concepts/inference|추론]] 수요를 폭발시키는 핵심 동력이 되고 있다.

## 핵심 기능 및 메커니즘
* **결정론적 데이터 접근**: 할루시네이션(환각)을 방지하기 위해 날것의 DB나 단순 텍스트-to-SQL에 의존하지 않고, [[wiki/concepts/semantic-layer]]에 사전에 정의된 엄격한 비즈니스 로직(지표, 차원, 필터 등)을 통해 정확한 수치를 추출한다.
* **분석 경로(KPI-Driver-Lever) 탐색**:
  * **KPI**: 분석의 목표가 되는 핵심 지표 (예: 과지급률, 이탈률).
  * **Driver**: 해당 지표에 직간접적으로 영향을 미치는 요인들 (예: 담당자, 보상 조직).
  * **Lever**: 기업이 실제로 통제하고 실행할 수 있는 개선 수단 (예: 특정 저성과 담당자와 유사 집단(Peer Group) 간의 실적 비교를 통한 코칭).
  에이전트는 이러한 경로가 시맨틱 레이어 등에 사전 정의되어 있을 때, 스스로 데이터를 좁혀나가며 원인을 분석하고 통찰을 제공한다.
* **스스로 보정하는 루프**: 생성한 쿼리가 실패하거나 예외가 발생할 경우, 에러 메시지를 읽고 쿼리 플랜을 스스로 수정하여 재시도하는 에이전틱 워크플로우(Agentic Workflow)를 갖춘다.
