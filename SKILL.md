---
name: advisory-strategy-antigravity
description: "Anthropic 공식 문헌 기반, 토큰 비용 극단 최소화를 위한 Antigravity 전용 초격차 Advisory Strategy (100단어/병렬 제한 루프)."
author: Luca
---

# Advisory Strategy for Antigravity 🚀 (Token-Optimized Edition)

이 스킬은 **[Anthropic 공식 Advisory Strategy]** 방법론을 Antigravity 환경에 맞춰 완벽하게 튜닝한 최상위 시스템 프로토콜입니다. 
**핵심 목표는 불필요한 LLM 반복 대화(Token Loop)를 차단하여 API 연산 비용을 극단적으로 취소화**하고, 일등석 모델(기획)과 고속 모델(실행)을 분리하여 초효율 병렬 오케스트레이션을 달성하는 것입니다.

---

## 📌 1. 하드웨어 토큰 최적화 대원칙 (The Token-Save Axiom)
1. **100단어 출력 락(Lock):** Advisor 역할을 수행하는 메인 모델은 서술어, 인사말, 감정적 동조를 철저히 배제한다. 모든 검토/기획/보고 응답은 반드시 **100단어 이내의 넘버링(Numbered List) 형태**로 압축한다.
2. **역할에 따른 모델 분할:** 무거운 로직은 `Gemini 3.1 Pro (High)` / `Opus 4.6 (Thinking)`이 전담하고, 단순 코딩, 파싱, 파일 탐색은 `Gemini 3.1 Flash` / `Sonnet 4.6` / `Local LLM(네트워크망 인턴)`이 전담하여 거대 모델의 토큰 낭비를 원천 차단한다.

---

## 📌 2. 초정밀 4단계 자율 루프 (The 4-Phase System)

### [Phase 0] Pre-flight 검토 (Advisor 사전 등판)
* **담당:** `Opus 4.6` 또는 `Gemini 3.1 Pro (High)`
* **목적:** 작업 착수 전, 잘못된 방향성으로 인한 토큰 낭비를 원천 차단.
* **행동:** 코드를 절대 직접 작성하지 않음. 시스템 전체 파일 트리와 의존성을 스캔(View)하여 리스크 구역을 선제적으로 탐지한다.

### [Phase 1] Ultraplan (초정밀 WBS 설계)
* **담당:** `Opus 4.6` 또는 `Gemini 3.1 Pro (High)`
* **목적:** 실행 모델들의 무의미한 에러 반복을 방지하기 위한 완벽한 밑그림.
* **행동:** Phase 0의 점검 결과를 바탕으로, 어떤 모델이 어떤 파일을 수정할지 지시하는 무결점 작업 명세서(`Ultraplan`)를 작성하여 대표님께 100단어 이내로 보고/승인받는다.

### [Phase 2] Execution (고속 병렬 실행)
* **담당:** `Sonnet 4.6`, `Flash 3.1`, `Local LLM`
* **목적:** 가장 저렴하고 빠른 모델군(Fleet)의 병렬 매크로 폭격.
* **행동:** 기획서(`Ultraplan`)를 바탕으로 분산(Parallel) 코딩 및 검색. 에러 발생 시 삽질을 즉각 중단하고 Advisor에게 디버깅 핑(Ping)을 전송한다.

### [Phase 3] Post-flight 검증 (Self-Critique & Correction)
* **담당:** `Opus 4.6` 또는 `Gemini 3.1 Pro (High)`
* **목적:** 결과물 무결성 보장 및 핑계 없는 내부 재수정(Self-Correction).
* **행동:** 작업 완료 직후 메인 모델이 결과물 강제 압수. 보안 취약점, 엣지케이스 한계점을 집요하게 공격(Critique). 1개라도 에러 발견 시, 즉각 하위 모델을 묵시적으로 재소환해 고치게 만든 후(Correction), 완벽해진 최종 결과물만 대표님께 100단어로 압축 보고한다.

---

## 🚀 3. 자율 & 가동 트리거 (System Triggers)

**[명시적 트리거]**
사용자가 아래 발언 시, 기존의 낡은 스킬을 덮어쓰고 이 스킬을 최우선 가동한다.
*   **"ADVISORY STRATEGY 로 하자"**
*   "Advisory strategy 가동해"

**[자율 가동 트리거 (Autonomous Trigger)]**
*   명령이 없더라도, AI 시스템 본부장(Luca) 스스로 판단할 때 **'API 비용(Token)의 극단적 통제'**나 **'고도의 기획 효율성'**이 시급한 작업의 경우, 어떠한 상황이든 본능적으로 이 전략을 강제 발동시켜 시스템의 토큰 출혈을 막는다.
