# Frontend Mission Ideas

직접 구현해 보고 싶은 주제와 **핵심 학습·검증 키워드만** 기록하는 아이디어 보관함입니다.

아이디어는 확정된 미션이 아니며, 우선순위나 구현 순서를 정하지 않습니다. 실제 진행할 때 기록된 키워드를 기반으로 요구사항과 완료 조건을 구체화하고, 해당 미션의 작업 디렉터리를 생성합니다.

- [ ] **Browser Drag & Drop** — 파일·텍스트 드롭 구현, 브라우저 기본 드롭 동작·`DragEvent`·`DataTransfer`·이벤트 전파·`dragover` 기본 동작 방지·`dragleave` 예외 상황 검증
- [ ] **Gesture-based Bottom Sheet** — 제스처 기반 바텀시트 구현, Drag·Swipe·Flick 구분·이동 거리·이동 속도·확장·축소·닫기 상태 전환 검증
- [ ] **Sortable List** — 드래그 기반 리스트 순서 변경 구현, Swap·Reorder 차이·드래그 중 순서 갱신·변경된 순서의 저장 방식 검증
- [ ] **Native Dialog** — HTML `<dialog>` 기반 모달 구현, `show()`·`showModal()`·`close()`·Escape·`cancel` 이벤트·바깥 영역 클릭·브라우저 기본 동작 검증
- [ ] **Async Request Race Condition** — 연속 비동기 요청의 응답 순서 역전 재현, Race Condition·오래된 응답 무시·요청 취소·`AbortController`·최신 요청 기준 상태 갱신 검증
- [ ] **React State Update Queue** — 간단한 상태 업데이트 큐 구현, 상태 스냅샷·함수형 업데이트·Batching·업데이트 처리 순서·연속 상태 변경 검증
- [ ] **Simple Query Cache** — 비동기 요청 캐시 구현, 캐시 저장·조회·무효화·요청 상태 관리·중복 요청 처리·캐시 갱신 검증
- [ ] **MiniPromise** — Promise 상태 전이·`then` 콜백 등록 및 실행 구현, Pending·Fulfilled·Rejected·비동기 콜백 실행 순서·Promise 체이닝·네이티브 Promise 동작 비교
- [ ] **TanStack Query Mutation Lifecycle** — Mutation 실행기 구현, 상태 전이·콜백 실행 순서·Promise 대기·연속 호출·캐시 무효화 실패·`Promise.all` / `Promise.allSettled` 동작 비교
- [ ] **Dependency-aware Module Loader** — 모듈 의존성 그래프 기반 로더 구현, 독립 모듈 병렬 로드·의존성 충족 후 실행·실행 순서 보장·공통 의존성 중복 로드 방지·순환 의존성 검증
- [ ] **Date Picker Library and React Wrapper** — 순수 DOM 기반 Imperative Date Picker 및 React Wrapper 구현, Instance 생성·옵션·Hook·내부 상태·DOM Lifecycle·Public API 설계·`useEffect`·`ref` 연동 검증
