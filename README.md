# Reactive Programming in iOS using Combine Framework
> Combine Framework 학습 내용 정리
<br>


<details>
  <summary>
    <h2>Introduction to Combine Framework</h2>
  </summary>
  
  <!-- 내용 -->
  - ### 1️⃣ Reactive Programming이란?
    > Reactive Programming은 비동기 데이터와 이벤트에 반응하고 이를 관리하는 데 중점을 두는 프로드래밍 패러다임으로, `선언적(declarative)`이고 `데이터 중심(data-driven)` 방식으로 이루어진다.
  
    - ### Key Concepts
      - **Observable**: 데이터 **이벤트를 제공(produces)하는** 엔티티
        - Examples: _User Input_, _Sensor Data_, _API Responses (XML or JSON, or Any kind of API)_
        
      - **Observer**: Observable에서 방출되는 **이벤트를 수신(listens)하는** 개체
        - Examples: _Application Components_, _Views_
        
      - **Operators**: 데이터를 **변환(transform)하고 조작(manipulate)하는** 함수
        - Examples: _map()_, _filter()_, _merge()_
      <br>
        
    - ### Benefits
      - 코드의 가독성이 향상
      - 복잡한 비동기 시나리오에 대한 함수 연산자를 통한 핸들링
      - 실시간 및 이벤트 기반 애플리케이션
      <br>
      
    - ### Reactive vs Imperative
      - ### Immutable v Mutable
        | Reactive Programming | Imperative Programming |
        |:---:|:---:|
        | 불변성을 강조 | 가변 변수 사용 |
        | 데이터 변경이 불가능. <br>변경 시, 새로운 상태(데이터) 생성 | 데이터 변경이 가능. <br>race condition 및 의도치 않은 변화(unintended changes)와 같은 잠재적 문제 발생 가능성 |
        | side effects의 위험을 감소, <br>동시 접근(concurrent access)을 간소화 |  |
        
      - ### Control Flow: Declarative v Explicit
        | Reactive Programming | Imperative Programming |
        |:---:|:---:|
        | 선언적 접근 | 단계별(step-by-step) 지침 |
        | `무엇(what)`을 해야 하는지에 초점 | loops와 conditionals를 포함한 `어떻게(how)`에 초점 |
        | 데이터 스트림의 변환으로 작업(operations)을 표현 |  |
        
      - ### Synchronous v Asynchronous
        | Reactive Programming | Imperative Programming |
        |:---:|:---:|
        | 비동기 작업 핸들링에 적합 | 일반적으로 동기적 |
        | 연산자(operators)를 사용하여 비동기 이벤트와 데이터 스트림을 효율적으로 관리 | 작업을 차단(Blocking operations)하면, <br> 높은 동시성을 요구하는 애플리케이션에서 병목 현상을 초래 |
        | 작업을 차단하지 않고(non-blocking), <br> 이벤트 중심의 처리가 가능 |  |
  <hr>
        
  - ### 2️⃣ Key concepts: Publishers, Subscribers, Operators, and Subjects
    - **Publishers**: `시간 경과에 따라 아이템을 방출`하는 데이터 소스
      - 데이터 스트림을 시작
      - Subscribers에게 데이터를 방출
      - Examples: _Sensors_, _API Endpoints_, _User Inputs_
        
    - **Subscribers**: Publishers가 방출한 `데이터를 수신하고 반응`함
      - 데이터 스트림을 수신
      - 방출된 아이템에 대해 응답 및 처리
      - Examples: _UI Components_, _Data Processor_
        
    - **Operators**: 데이터 스트림을 `변환`, `필터 또는 결합`하는 기능
      - Publisher로부터 방출된 데이터를 수정
      - 복잡한 데이터 조작 가능
      - Examples: _map_, _filter_, _merge_, _combineLatest_
        
    - **Subjects**: `Publisher`이면서 `Subscriber`인 특별한 타입
      - Publishers와 Subscribers의 브릿지 역할
      - 여러 Subscriber에게 데이터를 전송할 수 있음(Multicast)
      <br>

    - ### Use Cases
      - 실시간 데이터 스트리밍
      - 사용자 인터페이스 업데이트
      - 이벤트 기반 애플리케이션
      - 반응형 웹 서비스
      <br>

    - ### Benefits
      - 비동기, 이벤트 기반
      - 쉬운 데이터 조작
      - 확장성과 반응성
</details>
