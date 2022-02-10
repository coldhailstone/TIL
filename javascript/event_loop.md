# event loop
> <b>싱글 스레드</b> 기반 언어인 자바스크립트가 <b>멀티 스레드</b> 처럼 보이는 이유

[참조 영상](https://youtu.be/8aGhZQkoFbQ)

## 구조
- Call Stack
    - 코드가 실행될 때 쌓이는 곳
- Memory Heap
    - 메모리 할당이 일어나는 곳
- Web APIs
    - 브라우저에서 제공하는 API
- Callback Queue
    - 비동기 콜백 실행 전 보관하는 곳
    - Task Queue
    - Microtask Queue: Task Queue 보다 우선순위가 높음
- Event Loop
    - Call Stack이 비어있을 경우, Callback Queue에서 함수를 꺼내 Call Stack에 추가

## Run-to-Completion
- 자바스크립트가 실행되는 방식으로 콜 스택이 하나만 존재하기 때문에 진행중인 작업이 완전히 종료되야 다음 작업이 처리된다.

## 동작
1. 함수를 실행한다.
2. 실행된 함수가 Call Stack에 추가되어 처리된다.
3. 비동기 함수일 경우 브라우저에서 작업 후 Callback Queue 로 반환 한다.
4. Call Stack이 비어있다면 Event Loop가 반환된 콜백 함수를 Call Stack에 추가한다.