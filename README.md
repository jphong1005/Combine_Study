# Combine_Study

## Sections
<details>
  <summary>
    <h2>Introduction to Combine Framework</h2>
  </summary>
  
  <!-- 내용 -->
  - ### Reactive Programming이란?
    > Reactive Programming은 비동기 데이터와 이벤트에 반응하고 이를 관리하는 데 중점을 두는 프로드래밍 패러다임으로, `선언적(declarative)`이고 `데이터 중심(data-driven)` 방식으로 이루어진다.
    <br>
    
  - ### Key Concepts
    - **Observable**: 데이터 **이벤트를 제공(produces)하는** 엔티티
      > e.g. _User Input_, _Sensor Data_, _API Responses (XML or JSON, or Any kind of API)_
      
    - **Observer**: Observable에서 방출되는 **이벤트를 수신(listens)하는** 개체
      > e.g. _Application Components_, _Views_
      
    - **Operators**: 데이터를 **변환(transform)**하고 **조작(manipulate)**하는 함수
      > e.g. _map()_, _filter()_, _merge()_
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
      | operations 사용으로 데이터 스트림을 변환 |  |

</details>
