### HTML

#### HTML?
* 클라이언트와 서버의 통신에서 주고받는 파일
    * 이해가 쉬움
    * 정형화된 문법
    * 쓰이는 문법만 맨날 쓰임

* HTML(Hyper Text Markup Language) : 문서를 설명해준다.
    * Hyper Text = Link
    * Markup Language : 컴퓨터가 이해하는 언어
        * 프로그래밍 언어 X

#### HTML의 구조
1. 글               -> 글
2. 글을 감싸는 틀      -> 태그
3. 틀에 붙는 부가설명   -> 속성

- 태그의 종류를 나열하듯 외우며 공부하지 말고 문법형식과 동작방식에 집중합시다.

**코드**
```
제목 :
<h1></h1>
<h2></h2>

본문 : <p></p>

링크 : <a></a>

리스트 :
<li></li>
<ol></ol>
```

Introduction to html - [[과제](http://www.codecademy.com)]
1. 직접 쳐보는게 중요해요
2. HTML은 중요한 기초!

#### HTML 실습
**대원칙! : HTML로 꾸미려 들지 말자**
**꾸미는 언어는 CSS!**

1. "이거 HTML(로 작성된) 문서야~"를 알려주는 태그 :
    - <!DOCTYPE html>
    - <html lang='ko'>
    - <head>

2. 직접 화면에 등장하진 않지만 이 문서를 설명하는 태그
    - ex) 이 문서를 한 마디로 설명하는 문서의 'Title', 인코딩 방식(utf-8) 등등...

3. 직접적으로 화면에 등장하는 문서에서 보이는 태그
    - ex) h1,p,li,...

**실습**
[[index.html](index.html)]
- Vscode :
    - Extension : Live Server

##### Form 태그
* <form action ="전송받을대상"></form>
    * **사용자** -form-> **HTML** -form action="전송받을 대상"-> **전송 받을 대상**

##### Input 태그
* type : text,password,submit

**통신은 url로 이뤄진다.**

##### Select 태그
* option : value - 전송값 | text 보이는 값
* 리스트 생성

##### ol / ul / li 태그
* ex) ol>li*5
* ol : 순서있는 리스트 
* ul : 순서없는 리스트

##### a 태그
- <a href = "하이퍼링크"></a>