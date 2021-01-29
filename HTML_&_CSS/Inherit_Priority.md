### 상속과 우선순위

#### 상속
 - **부모나 조상에게 주어진 프로퍼티를 자식 혹은 후손 요소가 물려받는 것**

 - *모든 CSS 프로퍼티가 상속되는 것은 아님*
[[참조](http://www.w3.org/TR/CSS21/propidx)]

- 상속되지 않는 프로퍼티는 **inherit**으로 상속 가능
    - margin : inherit;

#### 우선순위
 - Cascading : CSS적용 우선순위
 - 규칙 :
    1. 중요도
        - CSS가 어디에 선언되었는지
            1. head 태그내의 style 태그
            2. head 태그내의 style 태그내의 @import문
            3. link 태그로 연결된 CSS
            4. link 태그로 연결된 CSS내의 @import문
            5. 브라우저 디폴트 Style

    2. 명시도
        1. !important : 세미클론 전에 사용
        2. 인라인 스타일(inline style) : 태그 내부에 style 선언
        3. 아이디 선택자(id selector)
        4. 클래스, 속성, 가상 클래스 선택자 (class, attribute, pseudo class selector)
        5. 태그 선택자(type selector)
        6. 전체 선택자(universal selector)
        7. 상속(inherit)

    3. 선언 순서
        * 나중에 선언된 스타일이 우선 적용
