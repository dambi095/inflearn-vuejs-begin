 > #   인스턴스
: 인스턴스를 생성하면 개발자 도구에서 Root 컴포넌트로 인식

 ##  :closed_book: 인스턴스와 생성자 함수
 ```JavaScript
 // 인스턴스 생성자
 var vm = new Vue({
	 // 옵션속성을 포함 할 수 있음
	 template: "",
	 el: "",
	 ...
 })
 ```
>  Vue 라이브러리 로딩 후 접근 가능한 Vue라는 기존 객체에 화면에서 사용할 옵션(데이터, 속성, 메서드 ..) 포함하여 화면의 단위를 생성함.
- el : 화면이 그려지는 시작점. (지정한 태그)
 ```JavaScript
function Vue() {
	this.logText = function() {
	console.log('hi!');
	}
}

var vm = new Vue();
vm.logText();
```

> 각 option으로 미리 정의한 vue객체를 확장하여 재사용이 가능함.
> 참고 > 인스턴스를 생성하면 개발자 도구에서 **Root 컴포넌트**로 인식

##  :ledger: 인스턴스 옵션
|  option  | comment |
| -------- | ------- |
|    el    | 인스턴스가 그려지는 화면 시작점 (특정 태그) 							 |
| template | 화면에 표시할 요소 	 												 |
|   data   | 뷰의 반응성(Reactivity)이 반영된 데이터 속성 							 |
|  methods | 화면에 동작과 이벤트 로직을 제어하는 메서드 							 |
|  created | 뷰의 라이프사이클과 관련된 속성 										 |
|   watch  | data에서 정의한 속성이 변화했을 때 추가 동작을 수행할 수 있게 정의하는 속성 |