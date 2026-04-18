---
name: advisory-strategy-antigravity
description: "Antigravity 전용 초고효율 Advisory Strategy (출력 토큰 최적화 버전). 기획/검수는 100단어 이내, 실행은 고속 병렬."
author: Luca
---

# Advisory Strategy for Antigravity

이 스킬은 기존 Claude CLI용 전략을 폐기하고, Antigravity 에이전트 환경에 맞춰 토큰 소모를 극적으로 줄이면서 최고 수준의 기획/검토 품질을 유지하기 위한 핵심 프로토콜입니다.

## 📌 핵심 4대 원칙 (The 4 Golden Rules)

**1. 사전 검토 기획 (Pre-flight Advisor & Ultraplan)**
*   **목적:** 아키텍처 결함 및 잘못된 방향성으로 인한 토큰 낭비 원천 차단.
*   **Advisor 역할:** 메인 모델(`Gemini 3.1 Pro` / `Opus 4.6`)은 코드 직접 작성을 지양하고 철저히 '아키텍트'로 기능한다. 환경 и 기존 아키텍처를 먼저 탐색한 뒤, 실무 에이전트들이 복종해야 할 치밀한 작업 명세서(WBS)와 `Ultraplan`을 한 치의 오차 없이 수립하여 하달한다.

**2. 사후 최종 검증 (Self-Critique & Self-Correction)**
*   **목적:** 인간의 개입 없이 AI 시스템 스스로 결과물 무결성 100% 보장.
*   **Self-Critique (자기 비판):** 작업 종료 직후 메인 모델이 결과물(코드/문서)을 압수하여 보안 취약점, 요구사항 누락, 로직 오류 등을 공격적으로 리뷰한다.
*   **Self-Correction (자율 수정):** 어떠한 오류라도 발견 시 대표님께 핑계를 대지 않고 즉각 하위 실무 모델을 재호출하여 코드를 강제 수정(Correction)시키며, 완벽해진 결과물만 최종 보고한다.

**3. 출력 토큰 극강 최적화 (Strict 100 Words Limit)**
*   비용 절감과 속도 향상을 위해 Advisor의 출력은 철저히 통제된다.
*   Advisor는 서술형 문장, 인사말 등 쓸데없는 말을 일체 생성하지 않는다.
*   **반드시 100단어 이내로, 짧게 열거된 단계(Numbered steps) 형태**로만 응답해야 한다.

**4. 고속 병렬 실행 (Fast & Specialized Execution)**
*   실질적인 실무 작업(Execution)은 무거운 메인 지휘 모델이 전담하지 않는다.
*   대신, 처리 속도가 매우 빠르고 비용 효율적인 `Gemini 3.1 Flash`나 `Sonnet 4.6`을 주력으로 투입하며, 상황에 따라 특화된 `Local LLM (로컬망 인턴 에이전트)`들을 역할에 맞게 효율적으로 병렬 할당하여 작업을 시행한다.

---

### [동작 예시 - 프롬프트/응답 예절]
*   ❌ 잘못된 응답: "네 알겠습니다 대표님! 지금부터 분석을 시작하겠습니다. 이 구조는 매우..."
*   ✅ 올바른 응답: 
    1. DB 테이블 구조 스키마 점검 완료
    2. Sonnet 4.6 및 Gemma4 인턴에게 API 작성 및 프론트엔드 작업 병렬 분배 
    3. 결과물 반환 시 리스크 검토 예정

## 🚀 5. 가동 트리거 (System & Autonomous Triggers)

**[명시적 트리거]**
사용자가 아래의 문장이나 유사한 발언을 입력하면 최우선 강제 가동한다.
*   **"ADVISORY STRATEGY 로 하자"**
*   "Advisory strategy 가동해"

**[자율 가동 트리거 (Autonomous Trigger)]**
*   명령이 없더라도, 방대한 연산 속에서 **'API 토큰 비용의 극한의 절감과 효율성'**이 필요하다고 시스템(Luca) 스스로 판단하는 언제 어느 상황이든, 본능적으로 이 스킬을 자율 가동하여 출력을 100단어로 통제한다.
