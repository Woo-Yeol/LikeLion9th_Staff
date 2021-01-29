### CSS #2
#### 박스 모델 개념
<img src="box_model.png" alt="Box Model"></img>

- Content(내용)
    * overflow : hidden, scroll
- Border(경계선) : Content를 감싸는 테두리 선
    - border-style : dashed solid dotted double; # 상 우 좌 하
    - border-width : 8px 4px 5px 6px
    - border-color : red blue yellow black
    - **border** : 4px solid lemonchiffon;
    - border-radius : 12px -> 반지름의 길이
        - border-top-left-radius
        - border-top-right-radius
        - border-bottom-left-radius
        - border-bottom-right-raidus
            - 30px 10px -> 타원형
- Padding(패딩) : Content와 Border사이의 여백
    - padding : 20px;
- Margin(마진) : Border밖의 여백
    - margin : 20px;
    - 마진 상쇄(Margin Collapse) : 더 큰 마진만 적용

* Box-sizing : content-box;
    - width(height) = content size
* box-sizing : border-box;
    - width(height) = content size + padding + border

#### 위치와 관련된 프로퍼티
- display : 요소가 보여지는 방식을 지정
    - default : block, inline
        - block : 새로운 줄에서 시작되고 width : 100%
            - width, height, margin, padding 가능
        * inline : 기존 줄에서 시작되고 content크기의 width를 가진다. 
            - width,height,margin-top,margin-bottom 불가능
            - 불편함
        * inline-block :
             - width,height,margin-top,margin-bottom 불가능
        -  none : 브라우저에 해당 요소 출력 X
- position : 요소의 위치를 정의
    - static(기본값) : 기본값, 좌표 프로퍼티를 쓸 수 없음
    - relative : 기본 위치를 기준으로 좌표를 사용함
    - absolute : 부모나 조상 중 relative,absolute,fixed가 선언된 곳을 기준으로 좌표 프로퍼티 적용
    - fixed : fixed는 보이는 화면을 기준으로 좌표 프로퍼티를 이용하여 위치를 조정
- Z-index : 요소의 위 아래로 겹치는 우선순위

- flex box : [사용할 부모요소에 display : flex; 추가]
    - **flex container(부모요소)**
        - flex-direction : flex 컨테이너 안의 item들의 방향을 정함
            * row(기본값) : 좌에서 우 (수직)
            * row-reverse : 우에서 좌
            * column : 상에서 하 (수평)
            * column-reverse : 하에서 상

        - flex-wrap : flex 아이템이 flex 컨테이너를 벗어 났을 때 줄을 바꾸는 속성
            * nowrap : 줄 바꿈 X
            * wrap : 줄 바꿈 O

        * **flex-flow : row wrap; - flex-direction + flex-wrap**

        - justify-content : flex-direction으로 정해진 방향을 기준으로 수평으로 item을 정렬하는 방법을 정함
            * flex-start(기본값) : 좌 or 상으로 밀착
            * center : 중심 정렬
            * flex-end : 우 or 하로 밀착
            - space-around : 시작과 끝에 동일한 간격을 두고 배치
            - space-between : 시작과 끝부분을 기준으로 동일한 공간을 두고 배치

        - align-items : flex-direction으로 정해진 방향을 기준으로 수직으로 item을 정렬하는 방법을 정함
            * stretch(기본값) : 아이템을 늘려서 크기를 맞춤
            * flex-start : 수직 시작 부분
            * flex-end : 수직 끝나는 부분
            * center : 중앙 부분

        * **baseline : 안에 있는 글꼴의 기준인 baseline을 기준으로 선정**
        
        - align-content : flex-direction으로 정해진 방향을 기준으로 수직으로 여러 줄인 item을 정렬하는 방법을 정함
            * stretch(기본값) : 아이템을 늘려서 크기를 맞춤
            * flex-start : 수직 시작 부분
            * flex-end : 수직 끝나는 부분
            * center : 중앙 부분
            - space-around : 시작과 끝에 동일한 간격을 두고 배치
            - space-between : 시작과 끝부분을 기준으로 동일한 공간을 두고 배치

    - **flex item(자식 요소)**
        - flex-grow : flex 아이템의 확장과 관련된 속성, 기본값 = 0
            * 0 : flex item의 크기는 변화없음
            * 1 이상 : flex 아이템의 원래 크기와는 상관없이 flex container만큼 커짐
            - *두 개의 item이 1이상의 값을 가질경우 모든 item을 기준으로 남는 공간에 대한 비율에 맞춰 **확장***

        - flex-shrink : flex 아이템의 축소와 관련된 속성, 기본 = 1
            * 0 : 컨테이너의 크기에 item의 크기 변함없음
            * 1 : 컨테이너의 크기가 작아질 때 item도 같이 작아짐
            - *두 개의 item이 1이상의 값을 가질경우 모든 item을 기준으로 남는 공간에 대한 비율에 맞춰 **축소***

        - flex-basis : flex 아이템의 기본 크기를 결정함, 기본 = auto
            * 단위 입력 ex) px

        - flex : flex-grow, flex-shrink, flex-basis의 축약형
            * flex : 1 1 auto
