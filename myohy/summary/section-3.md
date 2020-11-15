 > #   컴포넌트

 ##  :closed_book: 컴포넌트
> 조합하여 화면을 구성할 수 있는 블록(화면의 특정 역역)
> 화면영역을 단위별로 쪼개 **재사용**이 가능한 형태로 관리하기 위함

### ✍ 컴포넌트 등록

```JavaScript
 <!-- 전역 컴포넌트 등록 -->
 Vue.component('컴포넌트 이름', 컴포넌트 내용);

<!-- 지역 컴포넌트 등록 -->
var appHeader = {
	template: '<h1>Header</h1>'
}

new  Vue({
	el:  '#app', // 유일한 키값인 id로 선택
	// 지역 컴포넌트 등록 방식
	components: {
		// '컴포넌트 이름' : 컴포넌트 내용
		'app-footer': {
			template:  '<footer>footer</footer>'
		}
	}
})
 
```


##  :ledger: 컴포넌트와 인스턴스의 관계

#### *Compoenet.html 참고 
```
 Unknown custom element: <app-footer> - did you register the component correctly? 
 ```

> 지역 컴포넌트는 하단의 어떤 컴포넌트가 등록되어있는지 알수있음.
> 전역컴포넌트는 인스턴스를 생성할때마다 따로 등록할 필요가 없으나 지역컴포넌트는 인스턴스마다 새로 생성해줘야함

