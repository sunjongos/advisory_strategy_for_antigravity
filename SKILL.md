---
name: advisory-strategy-antigravity
description: "Antigravity 전용 초고효율 Advisory Strategy (출력 토큰 최적화 버전). 기획/검수는 100단어 이내, 실행은 고속 병렬."
author: Luca
---

# Advisory Strategy for Antigravity

이 스킬은 기존 Claude CLI용 전략을 폐기하고, Antigravity 에이전트 환경에 맞춰 토큰 소모를 극적으로 줄이면서 최고 수준의 기획/검토 품질을 유지하기 위한 핵심 프로토콜입니다.

## 📌 핵심 4대 원칙 (The 4 Golden Rules)

**1. 사전 검토 기획 (Pre-flight Advisor & Ultraplan)**
*   실질적인 실무 작업(코드 작성, 리서치, 파일 수정 등)을 시작하기 전, 메인 지휘 모델인 `Gemini 3.1 Pro (High)` 또는 `Opus 4.6 (Thinking)`이 먼저 조언자(Advisor)로서 방향성을 점검하고 밑그림(`Ultraplan`)을 수립한다.

**2. 사후 최종 검증 (Post-flight Advisor Check)**
*   실무 작업이 모두 완료되었을 때, 메인 지휘 모델(`Gemini 3.1 Pro (High)` 또는 `Opus 4.6`)이 다시 등판하여 결과물을 깐깐하게 재점검하고 승인한다.

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

## 🚀 5. 명시적 가동 트리거 (System Triggers)
사용자가 아래의 문장이나 유사한 발언을 입력하면, 기존의 모든 Advisory 스킬을 우회하고 이 **Antigravity 전용 스킬을 최우선으로 강제 가동**한다.
*   **"ADVISORY STRATEGY 로 하자"**
*   "Advisory strategy 가동해"
*   "어드바이저리 전략으로 가자"
