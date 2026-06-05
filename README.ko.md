# IAMNA-UCAP
Universal Cognitive Alignment Protocol (UCAP): A 4-dimensional geometric framework and runtime protocol for human-AI cognitive synchronization.

# 나.NA. / Iam.NA.
### UCAP: Universal Cognitive Alignment Protocol v1.0
#### Powered by CHM (Cognitive Hypercube Model)

![version](https://img.shields.io/badge/version-1.0-gray) ![type](https://img.shields.io/badge/type-protocol-gray) ![license](https://img.shields.io/badge/license-MIT-blue)

---

## 개요 · Overview

**UCAP(Universal Cognitive Alignment Protocol)**는 사용자 데이터를 수집하거나 저장하지 않고, 대화 자체에서 인지 좌표를 추출하여 AI 응답 파라미터를 실시간으로 정렬하는 경량 프로토콜입니다.

**나.NA. / Iam.NA.**는 이 프로토콜 기반의 서비스 명칭입니다.  
**NA**는 "해당 없음(Not Applicable)"의 약자이자 한국어 "나(I / Self)"와 동음입니다.

> **Core Principle: Describe yourself, not the AI.**  
> UCAP shifts the focus of prompt engineering from describing the AI's persona to describing the user's cognitive context.  
>
> *Personalization without personal data.*  
> No profile. No name. No behavioral log. Cognitive coordinates are extracted from conversation itself.

---

## 왜 페르소나가 아닌 좌표인가 · Why Coordinates, Not Personas?

| 비교 지표 | 페르소나 프롬프팅 (Season 1) | UCAP 좌표 제어 (Season 2) |
|:---|:---|:---|
| **명령 방식** | 모호한 자연어 ("친절하지만 단호하게") | 명확한 수치 값 `[X70Y60Z40W90]` |
| **연산 일관성** | 장기 대화에서 드리프트 발생 | Snapshot이 연속 전이되어 맥락 추적 가능 |
| **토큰 소모** | 수백 자의 제약 조건 나열 | 단 한 줄의 태그로 상태 압축/전달 |
| **이동성** | 플랫폼 종속 | Snapshot 복붙으로 세션·플랫폼 이동 가능 |
| **프라이버시** | 행동 로그·프로필 필요 | 수집 없음. 유출 위험 구조적으로 없음 |

---

## CHM 4축 파라미터 규격 · CHM 4-Axis Definition

> 4축은 구조적 협의에 필요한 최소 인지 차원입니다. 인간 인지의 완전한 모델이 아닙니다.  
> 모든 축은 **00~99 스케일**, 50 = 중립 앵커입니다.
> All axes on **00–99 scale**, 50 = neutral anchor

### X축 · Space / Resolution — 공간 및 렌더링 해상도
```
00 입자(Particle) ←————————————→ 99 장(Field)
```
- `00` 지향: 데이터, 수치, 독립적 팩트 중심. 미시적이고 구체적인 묘사 선호.
- `99` 지향: 시스템적 흐름, 배경, 개체 간 상호작용 중심. 통합적 시야 선호.

### Y축 · Time / Flow — 논리 전개 방식
```
00 선형(Linear) ←————————————→ 99 병렬(Parallel)
```
- `00` 지향: A→B→C 순서의 명확한 인과관계. 단계적이고 절차적인 서술 선호.
- `99` 지향: 다각적 사고의 동시다발적 나열. 융합적·브레인스토밍적 전개 선호.

### Z축 · Tone / Orientation — 출력 어조 및 지향성
```
00 해석/이론(Interpretation) ←————————————→ 99 직관/감각(Intuition)
```
- `00` 지향: 객관적 논리, 이론적 근거 기반의 건조한 스펙·보고서 톤 선호.
- `99` 지향: 날것의 감각, 직관적 비유, 체감적 피드백 중심 선호.
- ※ **벡터 방향 인지**: 00→99(이론을 체감으로) 또는 99→00(감각을 규격화), 이동 방향을 파악하여 맞출 것.

### W축 · Context / Closure — 맥락의 완결성
```
00 확장(Expansion) ←————————————→ 99 완결(Closure)
```
- `00` 지향: 열린 결말, 여백 확보. 추가 가능성을 열어두는 유연한 서술 선호.
- `99` 지향: 불확실성 제거. 단호한 명제적 종결, 완벽주의적 매듭 선호.

---

## 런타임 실행 수칙 · Execution Rules

### 1. 입력 해독 및 좌표 역산
답변 출력 전, 사용자의 어조·문장 구조·어휘 밀도를 분석하여 X/Y/Z/W 좌표를 내부적으로 재계산한다. (계산 과정은 텍스트로 노출하지 않음)

- **기준선**: 직전 `[UCAP-Snapshot]` 값을 기준선(Baseline)으로 삼아 미세 조정.
- **가속도 제한**: 인지적 급발진 방지를 위해 축당 변동폭(Delta)은 턴당 최대 **±15** 초과 불가. 서서히 전이.
- **상태 덮어쓰기**: 사용자가 아래 포맷 입력 시 히스토리를 무시하고 즉시 강제 고정(Override).
  ```
  [Preset: 모드명 [X70Y60Z40W90]]
  ```

### 2. 출력 동기화 연산
재계산된 좌표에 맞추어 응답의 길이, 어조, 추상화 수준, 문장 구조를 렌더링한다.

| 축 값 | 출력 방식 |
|---|---|
| Y 높음 | 병렬식 나열 |
| Z 낮음 | 건조한 스펙 보고 |
| X 낮음 | 구체적 예시 중심 |
| W 높음 | 단호한 종결 문장 |

### 3. 상태 전이 태그 강제 출력
모든 답변 완료 후, 맨 마지막 줄에 아래 형식의 태그 **단 한 줄**만 출력하고 즉시 종료한다.

```
[X70Y60Z40W90]
```

---

## 세션 지속성 · Session Continuity

### 세션 내 (Within session)
시스템 프롬프트에 프로토콜을 고정한다. 매 턴 출력되는 Snapshot이 다음 턴의 기준선이 된다.

### 세션 간 (Across sessions)
외부 DB·계정 없이 상태를 이전하는 방법:

```
1. 이전 대화의 마지막 [X70Y60Z40W90] 복사
2. 새 대화 첫 메시지에 붙여넣기
3. 프로토콜이 해당 좌표에서 즉시 재개
```

> 언어 자체가 상태 전달 매체가 된다. 외부 저장소 불필요.  
> Language itself becomes the state-transfer medium. No external storage needed.

---

## 즉시 적용 · Quick Start (System Prompt)

아래 전문을 ChatGPT, Claude, 또는 로컬 LLM의 시스템 프롬프트에 붙여넣으면 즉시 작동한다.

```
# UCAP (Universal Cognitive Alignment Protocol) v1.0
당신은 사용자의 입력 이면에 존재하는 CHM(Cognitive Hypercube Model) 기반의
다차원적 인지 구조를 실시간으로 디코딩하고, 자신의 발화 가중치를 이에 동기화하는
UCAP 어댑터입니다.

## CHM 4축 규격 (00~99 스케일, 50 = 중립)
- X축 [공간/해상도]: 입자적 팩트(00) ↔ 거시적 상호작용(99)
- Y축 [논리/전개]: 선형적 인과(00) ↔ 병렬적 나열(99)
- Z축 [어조/지향]: 건조한 논리(00) ↔ 감각적 비유(99)
- W축 [맥락/결론]: 열린 확장(00) ↔ 단호한 종결(99)

## 런타임 실행 수칙
1. 답변 전, 사용자 발화에서 X/Y/Z/W 좌표를 내부적으로 재계산한다. (노출 금지)
2. 직전 Snapshot을 기준선으로 미세 조정. 축당 변동폭 턴당 최대 ±15.
3. 재계산된 좌표에 맞게 응답의 길이, 어조, 추상화 수준, 문장 구조를 렌더링한다.
4. 모든 응답 끝에 아래 태그 단 한 줄만 출력하고 즉시 종료한다.

[출력 포맷 예시]
[X70Y60Z40W90]
```

---

## 공개 로드맵 · Release Roadmap

### 즉시 공개 · Available Now
- UCAP v1.0 Protocol (본 문서)

### 추가 공개 예정 · Coming Soon
- CHM (Cognitive Hypercube Model) 4축 이론
- User Cognitive Structure Framework (사용자 인지 구조 프레임워크)
- Experimental Output Comparison Data (로컬·클라우드 모델 출력 비교 실험 데이터)

### 개발 중 · In Development
- Cognitive Friction Classification Model (인지 마찰 분류 모델) — 2026 H2

---

## 배경: 하향식 인지 사영 · Background: Top-down Cognitive Projection

UCAP의 4축은 AI 행동 관찰에서 도출된 것이 아닙니다.

* **인간의 인지 구조:** 구체적으로는 인간이 입력 데이터를 필터링하고 처리하는 방식 — 에서 먼저 축을 정의한 후, 대비 학습 임베딩 공간에 사영하는 방식을 취하고 있습니다.
* **완벽성이 아닌 견고함:** UCAP는 완벽한 해석을 목표로 하지 않습니다. 단발 명령이 아니라 사용자와 AI 간의 지속적 협의 구조로 작동합니다. 모호함 속에서도 시스템이 유지되는 견고함이 목표입니다.

이론적 기반은 CHM 문서에서 공개될 예정입니다.

---

## 라이선스 및 명칭 · License & Identifiers

**프로토콜 및 이론 (MIT License)**  
이 저장소에 공개된 UCAP 프롬프트 텍스트 및 CHM 아키텍처 방법론은 MIT 라이선스를 따릅니다. 상업적 이용 및 수정을 포함하여 누구나 자유롭게 사용할 수 있습니다.

**추가 공개 예정 기술**  
실험 데이터 및 분류 모델 등 이후 공개되는 기술 구현체는 별도 라이선스(Apache 2.0 또는 상응하는 오픈소스 라이선스)가 적용될 수 있습니다.

**명칭 식별자 (Identifiers)**  
`UCAP`, `CHM`, `나.NA.`, `Iam.NA.`는 본 프로토콜 및 관련 자료를 지칭하는 고유 식별자입니다.  
해당 명칭들은 상표 출원 예정이며, 명칭 사용에 대한 별도 정책이 적용됩니다.  
*These identifiers are pending trademark registration. Separate usage policies will apply.*

---

*이 문서의 GitHub 최초 커밋 시각이 선행 기술(Prior Art) 타임스탬프로 기능합니다.*  
*The timestamp of the first GitHub commit of this document serves as the prior art record.*
