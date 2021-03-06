  # 싱글 파일 컴포넌트
> **싱글 파일 컴포넌트는 화면의 특정 영역에 대한 HTML, CSS, JS 코드를 한 파일에서 관리하는 방법**
  
   ##  :closed_book: 컴포넌트 등록
```
✔ template에는 루트 엘리먼트 하나만 있어야함!
<template>
	<div>
		<h1></h1>
		<div></div>
	</div>
</template>
```

``` 
✔ 컴포넌트의 재사용을 위해 다른 컴포넌트가 데이터를 공유하면 안되기 때문에 data를 정의할때는
export  default {
data: {
 ... 가 아니라
}

export  default {
data: function() {
	return { // 새 객체를 반환해줘야함
	}
  }
}
// 이런식으로 써야함
```

📄 컴포넌트 등록
> 컴포넌트 파일명은 파스칼케이스, 두 단어 이상으로 하는것이 좋음
	>> 한단어로 하면, 표준 태그와 충돌 날 수 있기 때문

appHeader --(등록)--> app
```js
import appHeader from './components/AppHeader';
// 컴포넌트 불러오기

...
export default {
components: { // 컴포넌트 등록
	'app-header' : AppHeader
}}
```

## :ledger:  props, emit

**[props]**
✔  **v-bind:프롭스 속성 이름(하위컴포넌트에서 받을 이름)="상위 컴포넌트의 데이터 이름"**

**[emit]**
✔  emit으로 하위 컴포넌트에서 데이터를 올리면
```js
methods: {
	sendEvent: function () {
	this.$emit('renew');  // 상위로 이벤트 전달
  }
}
```

✔ 상위컴포넌트에서 v-on으로 받아서 해당 메소드 실행
```js
v-on:renew="renewStr"
...
methods: {
	renewStr: function() {
	this.str  =  'hi'
}
```