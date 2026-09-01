# frontend-internals-missions

프론트엔드에서 자주 사용하는 추상화의 내부 동작을 **미션 → 탐색 → 설계 → 구현 → 검증 → 회고** 과정으로 학습하는 저장소입니다.

라이브러리의 사용법이나 정답 코드를 먼저 학습하기보다, 주어진 요구사항을 바탕으로 직접 문제를 해결하면서 각 추상화가 왜 필요한지 이해하는 것을 목표로 합니다.

---

## 학습 목적

React, JavaScript, 브라우저 생태계에는 개발자가 직접 구현하지 않아도 사용할 수 있는 많은 추상화가 존재합니다.

하지만 사용법만 알고 있으면 다음과 같은 질문을 만났을 때 내부 동작을 설명하기 어려울 수 있습니다.

* State Update Queue는 왜 필요한가?
* React의 State가 왜 현재 Render의 Snapshot으로 동작하는가?
* Functional Update는 왜 필요한가?
* Batching은 어떤 문제를 해결하는가?
* Stale Closure는 왜 발생하는가?
* Render와 Commit은 왜 분리되어 있는가?
* Query Cache와 Cache Invalidation은 왜 필요한가?
* Router는 어떤 문제를 추상화하는가?

이 저장소에서는 이런 개념을 단순히 암기하지 않고, 작은 기능을 직접 구현하며 다음 질문에 답할 수 있는 상태를 목표로 합니다.

> 왜 이런 구조가 필요한가?

> 어떤 문제를 해결하기 위해 이 추상화가 만들어졌는가?

> 내가 직접 구현한다면 어떤 구조로 설계할 것인가?

---

## 학습 방식

각 주제는 하나의 **Mission**으로 진행합니다.

Mission
→ 학습 목표 확인
→ 필요한 개념 조사
→ 직접 설계
→ 직접 구현
→ 테스트
→ 리뷰
→ 실제 구현과 비교
→ 회고

정답 구현을 먼저 확인하지 않습니다.

먼저 학습 목표와 외부에서 관찰 가능한 요구사항만 확인한 뒤, 필요한 자료구조와 구현 방법을 직접 결정합니다.

구현을 완료한 이후 실제 라이브러리의 구조나 다른 구현과 비교하며 차이와 Trade-off를 확인합니다.

---

## AI 사용 원칙

AI는 구현을 대신하는 도구보다 **미션 출제자와 리뷰어**로 사용합니다.

### 구현 전

AI에게 요청할 수 있는 것

* 학습 목표
* 선행 학습 개념
* 동작 요구사항
* 테스트 시나리오
* 완료 기준
* 회고 질문

AI에게 요청하지 않는 것

* 구현 코드
* 의사 코드
* 자료구조 선택
* 함수 및 객체 구조
* 실제 라이브러리 내부 구현
* 직접적인 해결 방법

### 구현 후

구현을 완료한 뒤에는 AI를 활용해 다음을 검증합니다.

* 놓친 Edge Case
* 설계상의 문제
* 실제 구현과의 차이
* Trade-off
* 기술 면접 질문
* 설명이 부족한 개념

가능하면 정답을 바로 확인하기보다, 질문을 통해 문제를 스스로 발견하는 방식을 우선합니다.

---

## Mission Structure

각 Mission은 다음과 같은 구조로 관리합니다.

missions/
├── 01-state-update/
│   ├── README.md
│   ├── src/
│   └── retrospective.md
├── 02-render-snapshot/
│   ├── README.md
│   ├── src/
│   └── retrospective.md
└── ...

### Mission README

각 Mission의 README에는 다음 내용을 기록합니다.

* 학습 목표
* 선행 개념
* 요구사항
* 제약 조건
* 테스트 시나리오
* 완료 기준

### Retrospective

구현 이후에는 다음 내용을 회고합니다.

* 처음 예상한 구조
* 실제 구현 구조
* 구현하면서 막힌 부분
* 선택한 방법과 이유
* 고려했던 다른 방법
* 현재 구현의 한계
* 실제 라이브러리와의 차이
* 새롭게 이해한 개념
* 다시 구현한다면 바꿀 점

---

## Missions

필요한 주제를 순차적으로 추가합니다.

### React State & Rendering

* [ ] State Snapshot
* [ ] State Update Queue
* [ ] Functional Update
* [ ] Batching
* [ ] Stale Closure
* [ ] Hook State
* [ ] Render / Commit
* [ ] Reconciliation
* [ ] Scheduling / Priority

### JavaScript & Browser

* [ ] Closure
* [ ] Event Loop
* [ ] Task / Microtask
* [ ] Promise
* [ ] Debounce
* [ ] Throttle

### Application Architecture

* [ ] Client-side Router
* [ ] Pub/Sub Store
* [ ] Query Cache
* [ ] Cache Invalidation
* [ ] Mutation Lifecycle

---

## Mission 완료 기준

코드가 동작하는 것만으로 Mission을 완료하지 않습니다.

다음 질문에 자신의 언어로 답할 수 있어야 완료한 것으로 봅니다.

1. 어떤 문제를 해결하기 위해 이 구조가 필요한가?
2. 내가 선택한 자료구조와 설계는 무엇인가?
3. 왜 그 방법을 선택했는가?
4. 다른 방법으로 구현할 수 있는가?
5. 현재 구현의 한계는 무엇인가?
6. 실제 라이브러리는 이 문제를 어떻게 해결하는가?
7. 실제 프로젝트에서는 언제 이 개념이 중요해지는가?

---

## 원칙

> 구현 자체보다 추상화가 만들어진 이유를 이해한다.

> 정답을 먼저 보기보다 문제를 먼저 경험한다.

> 동작을 외우기보다 자신의 언어로 설명할 수 있는 상태를 만든다.

> AI가 사고를 대신하지 않고, 사고를 검증하도록 사용한다.
