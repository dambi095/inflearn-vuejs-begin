#  템플릿문법
  > 뷰로 화면을 조작하는 방법
  
   ##  :closed_book: 데이터바인딩
> 뷰 인스턴스에서 정의한 속성들을 화면에 표시하는 방법 ex. 콧수염괄호(Mustache Tag) = 보간법
``` <div>{{ message }} </div>```

   ##  :ledger: 디렉티브
   >  html태그에서 표준 속성을 제외하고 'v-' 라고 붙은 속성들로 v-가 붙으면 뷰 내부적으로 인식항 돌아감
   >  ex. v-bind, v-on ...

   **값 변화에 따라 실시간으로 html돔에 바인딩한 값도 실시간으로 변화함.**

### ✍ v-bind (약어 ':')
-  **태그의 속성값을 바인딩 해줌**
- **v-bind:태그명="바인딩할 값"**
	- 브라우저가 v-bind를 만나게 되면 vue를 뒤져 값을 찾아 바인딩

### ✍ v-if / v-else-if / v-else , v-show
- **조건문**
```js
<!-- 유저가 로그인하기전 로딩상태 -->
<div  v-if="loading"> 
	Loading ...
</div>
<!-- 로그인 된 후의 상태 -->
<div  v-else> 
	test user has been logged in
</div>
<!-- v-show -->
<div  v-show="loading">Loading show test</div>
```
- loading을 체크해제 했을 때, 
	- v-if는 돔자체를 지우고, v-show는 화면에 보이지 않을 뿐(style="display:none;") 돔엔 남아있음

 :speech_balloon: **참고**
- [공식문서](https://vuejs.org/v2/guide/forms.html#ad)

### ✍ v-model
- **input과 textarea 엘리먼트에 양방향데이터바인딩 해줌**
-> 모든 폼 엘리먼트 초기 value 와 checked, selected 속성을 무시하며 항상 **vue인스턴스데이터를 원본소스**로 취급함
-> 컴포넌트의 data 옵션 안에 있는 JavaScript 에서 초기값을 선언해야 함

### ✍ v-on (약어 '@')
- **이벤트 등록할때 사용**
- **v-on:이벤트="이벤트 발생시 수행될 메소드명"**
```html
	<button v-on:click=""></button>
	<button @click=""></button>