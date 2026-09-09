# frontend-implementation-missions

작은 프론트엔드 문제를 **미션 → 분석 → 설계 → 구현 → 검증 → 회고** 과정으로 직접 해결하며 구현 능력을 훈련하는 저장소입니다.

정답 코드나 특정 구현 방식을 먼저 학습하기보다, 주어진 요구사항을 바탕으로 직접 문제를 분석하고 설계하며 해결하는 것을 목표로 합니다.

일부 미션에서는 React, JavaScript, 브라우저 및 라이브러리가 제공하는 추상화를 낮은 단계에서 직접 구현하며 내부 동작과 추상화가 만들어진 이유도 탐구합니다.

---

## 학습 목적

프론트엔드 개발에서는 API와 라이브러리의 사용법을 아는 것뿐만 아니라, 요구사항을 코드 구조로 변환하고 직접 구현하는 능력이 필요합니다.

이 저장소에서는 작은 미션을 반복하며 다음 능력을 훈련합니다.

- 요구사항을 분석하고 필요한 동작을 식별하기
- 상태와 데이터 흐름을 직접 설계하기
- 컴포넌트와 함수의 책임을 나누기
- JavaScript / TypeScript로 로직 구현하기
- React의 상태와 렌더링을 고려해 구현하기
- DOM / Browser API를 직접 다루기
- 비동기 요청과 에러 상황 처리하기
- 버그의 원인을 추적하고 수정하기
- 구현한 구조의 한계와 Trade-off 설명하기

단순히 기능이 동작하는 것을 넘어 다음 질문에 자신의 언어로 답할 수 있는 상태를 목표로 합니다.

> 왜 이런 구조로 구현했는가?

> 다른 방법으로 구현할 수 있는가?

> 현재 구현의 한계는 무엇인가?

> 사용한 추상화는 어떤 문제를 해결하고 있는가?

---

## 학습 방식

각 주제는 하나의 **Mission**으로 진행합니다.

```text
Mission
→ 요구사항 분석
→ 직접 설계
→ 직접 구현
→ 테스트 및 디버깅
→ 검증
→ 회고
```

미션에서는 외부에서 관찰 가능한 요구사항과 제약조건을 기준으로 구현합니다.

구현 과정에서 다음과 같은 판단을 직접 수행합니다.

- 어떤 상태가 필요한가?
- 데이터는 어떤 방향으로 흐르는가?
- 어떤 책임을 분리해야 하는가?
- 어떤 자료구조와 API가 적절한가?
- 어떤 예외 상황을 처리해야 하는가?

구현 과정에서 필요한 개념은 실제 문제와 연결하여 학습합니다.

---

## Mission 유형

Mission은 특정 분야에 한정하지 않습니다.

### UI & Interaction

사용자 인터랙션과 UI 상태를 구현합니다.

예:

- Searchable List
- Modal
- Tabs
- Dropdown
- Pagination
- Infinite Scroll
- Form Validation
- Keyboard Navigation
- Focus Management

### React State & Rendering

React의 상태와 렌더링 특성을 고려한 구현을 연습합니다.

예:

- Derived State
- Async State
- Effect Lifecycle
- Stale Closure
- Optimistic UI
- Component Responsibility
- Render Performance

### JavaScript & Browser

JavaScript와 브라우저가 제공하는 기본 기능을 직접 다룹니다.

예:

- Closure
- Event Loop
- Promise
- Debounce
- Throttle
- DOM Event
- IntersectionObserver
- AbortController
- History API
- Web Storage

### Async & Data

비동기 요청과 데이터 상태를 직접 관리합니다.

예:

- Request State
- Request Cancellation
- Race Condition
- Retry
- Pagination
- Cache
- Optimistic Update

### Frontend Internals

이미 사용하고 있는 추상화를 낮은 단계에서 직접 구현하며 내부 원리를 탐구합니다.

예:

- State Snapshot
- State Update Queue
- Functional Update
- Batching
- Hook State
- Pub/Sub Store
- Client-side Router
- Query Cache
- Cache Invalidation
- Reconciliation

이 유형에서는 구현 자체뿐만 아니라 다음 질문도 함께 탐구합니다.

> 왜 이 추상화가 필요한가?

> 어떤 문제를 해결하기 위해 만들어졌는가?

> 실제 라이브러리에서는 어떤 부분을 추가로 고려하는가?

---

## Repository Structure

각 Mission은 독립적인 단위로 관리합니다.

```text
missions/
├── 01-search-list/
│   ├── README.md
│   ├── src/
│   └── retrospective.md
├── 02-async-request/
│   ├── README.md
│   ├── src/
│   └── retrospective.md
├── 03-state-update-queue/
│   ├── README.md
│   ├── src/
│   └── retrospective.md
└── ...
```

큰 애플리케이션을 완성하는 것보다 하나의 구현 문제를 작은 범위에서 집중적으로 다루는 것을 우선합니다.

---

## Mission README

각 Mission의 README에는 구현 전에 필요한 내용을 기록합니다.

- 상황
- 학습 목표
- 요구사항
- 제약조건
- 테스트 시나리오
- 완료 조건

구현 방법이나 정답 구조는 미리 기록하지 않습니다.

---

## Retrospective

구현 이후에는 구현 과정에서 중요했던 판단을 기록합니다.

- 처음 예상한 구조
- 실제 구현 구조
- 구현하면서 막힌 부분
- 선택한 방법과 이유
- 고려했던 다른 방법
- 현재 구현의 한계
- 새롭게 이해한 개념
- 다시 구현한다면 바꿀 점

Frontend Internals 성격의 Mission에서는 필요에 따라 다음 내용도 추가합니다.

- 실제 라이브러리 또는 프레임워크와의 차이
- 해당 추상화가 해결하는 문제
- 실제 구현에서 추가로 고려하는 요소

---

## Missions

Mission은 정해진 순서를 모두 수행하기보다 현재 필요한 구현 능력에 따라 추가합니다.

### UI & Interaction

- [ ] Searchable List
- [ ] Modal
- [ ] Tabs
- [ ] Dropdown
- [ ] Pagination
- [ ] Infinite Scroll
- [ ] Form Validation
- [ ] Keyboard Navigation

### React State & Rendering

- [ ] Derived State
- [ ] Async State
- [ ] Effect Lifecycle
- [ ] Stale Closure
- [ ] Optimistic UI
- [ ] Component Responsibility
- [ ] Render Performance

### JavaScript & Browser

- [ ] Closure
- [ ] Event Loop
- [ ] Task / Microtask
- [ ] Promise
- [ ] Debounce
- [ ] Throttle
- [ ] AbortController
- [ ] IntersectionObserver
- [ ] History API

### Async & Data

- [ ] Request State
- [ ] Request Cancellation
- [ ] Race Condition
- [ ] Retry
- [ ] Pagination
- [ ] Cache
- [ ] Optimistic Mutation

### Frontend Internals

- [ ] State Snapshot
- [ ] State Update Queue
- [ ] Functional Update
- [ ] Batching
- [ ] Hook State
- [ ] Render / Commit
- [ ] Reconciliation
- [ ] Scheduling / Priority
- [ ] Client-side Router
- [ ] Pub/Sub Store
- [ ] Query Cache
- [ ] Cache Invalidation
- [ ] Mutation Lifecycle

---

## Mission 완료 기준

코드가 동작하는 것만으로 Mission을 완료하지 않습니다.

구현 이후 최소한 다음 내용을 자신의 언어로 설명할 수 있어야 합니다.

1. 어떤 요구사항을 해결했는가?
2. 어떤 구조로 구현했는가?
3. 왜 이 구조를 선택했는가?
4. 구현하면서 어떤 문제가 발생했는가?
5. 현재 구현의 한계는 무엇인가?
6. 다른 방법으로 구현할 수 있는가?

내부 추상화를 다루는 Mission에서는 추가로 확인합니다.

7. 이 추상화는 어떤 문제를 해결하기 위해 존재하는가?
8. 실제 라이브러리에서는 이 문제를 어떻게 다루는가?

모든 항목을 매번 문서화하는 것보다, 구현 과정에서 내린 판단을 스스로 설명할 수 있는 상태를 중요하게 봅니다.

---

## 원칙

> 정답을 먼저 보기보다 문제를 먼저 경험한다.

> 작은 기능이라도 직접 분석하고 설계하고 끝까지 구현한다.

> 코드가 동작하는 것뿐만 아니라 왜 그렇게 구현했는지 설명할 수 있어야 한다.

> 모르는 개념은 실제 구현 문제와 연결해서 이해한다.

> 추상화를 사용할 때는 필요에 따라 그 아래에서 어떤 문제가 해결되고 있는지도 탐구한다.
