### HTML 기초 문법

#### 요소와 태그
|태그|요소|
|:--:|:--:|
|```<h1></h2>```|제목입니다.|

#### 구조
* ```<!DOCTYPE html>``` : 문서 형식을 정의
* ```<html lang= 'kr'></html>``` : 주 언어가 한국어(접근성을 위한 표기)임을 정의 및 본격적 태그의 시작

#### Head와 Body에 들어갈 요소
* ```<head></head>```
    * ```<meta></meta>``` : 문서와 관련된 정보를 담음
        * charset = "ko"
    * ```<title></title>```
        * Tab 이름 설정

* ```<body></body>```

#### 레이아웃과 관련된 기본 태그
* 레이아웃 :
    * 시멘틱 태그(Semantic tag) : 의미를 가지고 있는 태그
        * header : 소개와 제목을 담음
        * nav : 네비게이션 역할 - 페이지 이동을 위한 메뉴
        * section : 기준에 맞게 구간 나눔
            * article : 주 내용을 담기 위한 요소
        * aside : 광고나 사이트의 주변 부분을 담기위한 요소
        * footer : 웹 사이트 아래 부분에 위치, 회사 & 정보등의 추가 정보를 담기 위해 사용하는 요소

#### 텍스트와 관련된 태그
* 콘텐츠 : 영상과 이미지, 텍스트
* 제목 태그 : 제목을 나타내고 싶을 때 사용
    * h1~h6
* 본문 태그 : 
    * p(arahraph) : 단락, 문단 (줄바꿈을 해도 띄어쓰기로 인식)
    * br(eak) : 줄바꿈 - **빈 요소(empty element)**
    * pre(formatted) : 입력한 그대로 출력 (들여쓰기, 줄바꿈 주의) 
    * 아무런 태그가 없는 본문도 태그가 있는 것처럼 출력

#### 글자와 관련된 태그
* strong : Bold체
* em(phasize) : italic체
* sub(scripted) : 일반 위치보다 아래에 기입
* sup(erscripted) : 일반 위치보다 위에 기입
* ins(ert) : 밑줄
* del(ete) : 취소선

#### 링크 태그
* <a></a> : anchor(닻)
    * attributes : 태그에 대해 추가적인 정보 제공 / HTML의 모든 태그는 속성을 가질 수 있음
        * 키 = '값'
    * href = "url"
        * hypertext reference
    * Url(Uniform Resource Locator) = Address + Path
        * 인터넷에서 HTML페이지, CSS 문서, 이미지 등 자원(Resource)의 위치를 나타냄
        * 절대 URL(Absolute URL) : 접근하는 최초 시작점부터 경유한 경로를 모두 기록하여 리소스의 위치를 나타냄
        * 상대 URL(Relative URL) : 기준적ㅁ을 기준으로 상대적인 경로를 기록하여 리소스의 위치를 나타냄
    * target : 클릭으로 링크를 열 때 어디에 오픈 할 것 인지 정하는 속성
        * "_self" : 현재 창
        * "_blank" : 새 창

#### 이미지 태그
* ```<img src="이미지 url">```
    * src="이미지 url" : 불러올 이미지의 URL을 속성 값으로 가짐 src는 Source(근원)의 약자
    * alt="사진설명" " alternative text / 불러올 이미지가 없거나 불러오는데 실패했을 경우 대신 표시되는 문장
    * width = "수치", height="수치"
* **유튜브**
    * 공유하기 -> 퍼가기 -> ```<iframe src="https://www.youtube.com/embed/[유튜브 영상 ID]"></iframe>```

#### 테이블
* 테이블의 구성 :
    * 표 - ```<table></table>``` : 표 전체를 감싸는 태그
        * ```<tr>``` : 표에서 행을 구분하는 태그
        * ```<th>``` : 표의 행 내부에서 제목 셀을 담는 태그
        * ```<td>``` : 표의 행 내부에 데이터 셀을 담는 태그
        * rowspan='숫자' : '숫자'만큼 셀이 행을 점유
        * colspan='숫자' : '숫자'만큼 셀이 열을 점유

**예시**

|성별|학년|이름|
|:--:|:--:|:--:|
|남|3|수노|
|여|3|곽두팔|
```
<table>
    <tr>
        <th>성별</th>
        <th>학년</th>
        <th>이름</th>
    </tr>
    <tr>
        <td>남</td>
        <td>3</td>
        <td>수노</td>
    </tr>
    <tr>
        <td>여</td>
        <td>3</td>
        <td>곽두팔</td>
    </tr>
</table>
```

**예시**
|성별|남|여|
|:--:|:--:|:--:|
|학년|3|3|
|이름|수노|곽두팔|
```
<table>
    <tr>
        <th>성별</th>
        <td>남</td>
        <td>여</td>
    </tr>
    <tr>
        <th>학년</th>
        <td>3</td>
        <td>3</td>

    </tr>
    <tr>
        <th>이름</th>
        <td>수노</td>
        <td>곽두팔</td>
    </tr>
</table>
```

**예시**
|성별|남|여|
|:--:|:--:|:--:|
|학년|3|
|이름|수노|곽두팔|
```
<table>
    <tr>
        <th>성별</th>
        <td>남</td>
        <td>여</td>
    </tr>
    <tr>
        <th>학년</th>
        <td colspan="2">3</td>
    </tr>
    <tr>
        <th>이름</th>
        <td>수노</td>
        <td>곽두팔</td>
    </tr>
</table>
```

#### 목록 태그
* ul(Unordered List) / ol(Ordered List) / li(List item) : 순서없는 / 순서있는 / 목록
    * ol :
        * start='숫자' : 리스트가 시작하는 숫자를 정함
        * type='문자' : 순서를 시작하는 문자를 정함
        * reversed : 순서를 반대로 시작 / 다른 속성과 달리 Key만 사용
    * li :
        * value='숫자' : 해당하는 리스트 아이템의 번호를 지정

**예시**
```
<ul>
    <li>맛집탐방</li>
        <ol start="3" type="I" reversed>
            <li value="5">1</li>
            <li value="8">2</li>
        </ol>
    <li>놀러가기</li>
</ul>
```

#### Form 태그
* ```<form>``` : 폼에 포함되는 다양한 입력 양식 태그 들을 감싸줌
    * action : 데이터를 보낼 URL을 지정
    * method : 보내는 방식을 지정
        * method='get' : 데이터를 URL 끝에 붙여 눈에 보이게 보냄
            1. 데이터 조회만을 목적으로 할 때 주로 쓰임
            2. 데이터 검색어 방식 
        * method='post' : 데이터를 URL에 적지 않고 내부에 숨겨서 보냄
            1. 서버에 있는 데이터를 쓰거나 수정,삭제를 할 때 주로 사용

#### Textarea
* ```<textarea>``` : 한 번에 많은 글을 입력받을 때 사용

#### Button
*  ```<input type ="button" value = "회원가입"> = <button type="submit">회원 가입</button>```

#### 회원가입 폼 예시
**회원가입 폼**
```
 <form action="" method="get">
    <div>
        <label for="userid">아이디 :</label>
        <input type="text" id = "userid" name="id" placeholder="아이디를 입력해주세요" value="snow">  <--!도메인?id=####-->
    </div>
    <div>
        <label for="userpw">비밀번호 :</label>
        <input tyep="password" id="userpw" name="password" placeholder="비밀번호를 입력해주세요">
    </div>
    <div>
        <label for="gender">성별 : </label>
        <select name="gender" id="gender">
            <option value="male">남성</option>
            <option value="female">여성</option>
        </select>
    </div>
    <div>
        <label for="introduce">자기소개 : </label>
        <textarea for="introduce" cols="30" rows="10" placeholder="자기소개를 입력하세요."></textarea>
    </div>
    <button type="submit">제출</button>
    <button type="reset">리셋</button>
 </form>
```

