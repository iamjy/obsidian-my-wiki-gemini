---
title: "시맨틱 레이어 (Semantic Layer)"
date: 2026-05-10
tags: [data, semantic-layer, bi, ai-agent, concept]
type: concept
status: active
source: "[[wiki/ingests/2026-05-10-ai-agent-kpi-decision]]"
related: ["[[wiki/concepts/decision-agent]]"]
---

# 시맨틱 레이어 (Semantic Layer)

**시맨틱 레이어(Semantic Layer)**는 물리적인 데이터베이스(또는 데이터 웨어하우스)와 최종 데이터 소비자(비즈니스 사용자, BI 도구, AI 에이전트 등) 사이에 위치하여, 복잡한 데이터 구조를 비즈니스 친화적인 용어와 로직으로 매핑해주는 중간 계층이다. 의미 계층이라고도 부른다.

## 핵심 역할
* **비즈니스 로직의 중앙화**: '활성 고객', '수익률', '이탈률' 등 조직 내에서 쓰이는 핵심 성과 지표(KPI)와 비즈니스 용어의 정의(계산식, 필터, 조인 규칙 등)를 한 곳에서 관리하여 단일 진실 공급원(Single Source of Truth)을 제공한다.
* **추상화**: 복잡한 물리적 테이블 구조나 SQL 문법을 몰라도 데이터를 조회할 수 있도록 한다. (예: `SELECT * FROM table_A JOIN table_B...` 대신 `활성 고객 수와 지역별 매출을 보여줘` 형태의 쿼리를 가능하게 함)

## AI 에이전트 시대의 중요성
* 단순 Text-to-SQL 모델은 스키마가 복잡해질수록 환각(Hallucination)과 부정확한 쿼리를 생성할 확률이 급격히 높아진다.
* AI 에이전트가 직접 DB를 탐색하는 대신 시맨틱 레이어를 통해 제공되는 일관된 메타데이터(지표, 차원 등)를 바탕으로 쿼리를 구성(예: 시맨틱 MCP 활용)하게 하면, 답변의 정확성을 100%에 가깝게 통제하고 신뢰성 있는 데이터 분석을 수행할 수 있다.
