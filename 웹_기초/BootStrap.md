### Bootstrap

#### BootStrap이란?
* 트위터의 개발자가 만든 CSS / JS 기반의 웹 프레임워크
* Open Source
* 반응형 웹 지원 (자동 화면 조정)
* 브라우저 호환성
* 성능이 다소 떨어짐


#### 실습
[[Just.html](./just.html)]
1. 부트스트랩 CDN :
    - head에 추가하기
2. Jquery CDN :
    - head에 추가하기
3. 부트스트랩의 콘테이너 만들기
    -  <pre><code><div class="container"></div></code></pre>
4. 부트스트랩의 버튼 적용하기
    -  <pre><code><input type="submit" class="btn btn-primary"></code></pre>
5. 부트스트랩의 폼 가져오기
```
<form action="전송받을대상">
        아이디 : <input type="text" name="id">
        비밀번호 : <input type="password" name="pw">
        <div class="form-group">
          <label for="exampleInputEmail1">이메일 주소</label>
          <input type="email" class="form-control" id="exampleInputEmail1" placeholder="이메일을 입력하세요">
        </div>
        <div class="form-group">
          <label for="exampleInputPassword1">암호</label>
          <input type="password" class="form-control" id="exampleInputPassword1" placeholder="암호">
        </div>
        <div class="form-group">
          <label for="exampleInputFile">파일 업로드</label>
          <input type="file" id="exampleInputFile">
          <p class="help-block">여기에 블록레벨 도움말 예제</p>
        </div>
        <div class="checkbox">
          <label>
            <input type="checkbox"> 입력을 기억합니다
          </label>
        </div>
        <button type="submit" class="btn btn-primary">제출</button>
</form>
```

6. 부트스트랩의 nav 가져오기
```
<ul class="nav nav-tabs">
  <li role="presentation" class="active"><a href="#">Home</a></li>
  <li role="presentation"><a href="#">Profile</a></li>
  <li role="presentation"><a href="#">Messages</a></li>
</ul>
```
7. 부트스트랩의 그래프 가져오기
```
    <div class="progress">
        <div class="progress-bar progress-bar-success" role="progressbar" aria-valuenow="40" aria-valuemin="0" aria-valuemax="100" style="width: 40%">
          <span class="sr-only">40% Complete (success)</span>
        </div>
      </div>
      <div class="progress">
        <div class="progress-bar progress-bar-info" role="progressbar" aria-valuenow="20" aria-valuemin="0" aria-valuemax="100" style="width: 20%">
          <span class="sr-only">20% Complete</span>
        </div>
      </div>
      <div class="progress">
        <div class="progress-bar progress-bar-warning" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100" style="width: 60%">
          <span class="sr-only">60% Complete (warning)</span>
        </div>
      </div>
      <div class="progress">
        <div class="progress-bar progress-bar-danger" role="progressbar" aria-valuenow="80" aria-valuemin="0" aria-valuemax="100" style="width: 80%">
          <span class="sr-only">80% Complete (danger)</span>
        </div>
      </div>
```