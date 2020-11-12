> #   컴포넌트 통신 방법

 ##  :closed_book: 컴포넌트 통신
> * 뷰 컴포넌트는 데이터유효범위(scope)를 갖음.
> * 각 컴포넌트의 유효 범위가 독립적이기 때문에 다른 컴포넌트의 값을 직접적으로 참조할 수가 없음
> *  n방향 통신의 문제점 : 특정상태, 데이터이 바꼇을때 그로인한 버그를 추적하기 어려움

![component](https://joshua1988.github.io/vue-camp/assets/img/component-communication.2bb1d838.png)

- **props** : 상위 -- (데이터내려줌) --> 하위 
- **event emit** : 하위 -- (이벤트올려줌) --> 상위 

---

##  :ledger: Props 
###  ✍ props 속성 코드 형식 
- ```상위 --> 하위 ``` : <app-header v-bind: 프롭스 속성 이름 = "상위 컴포넌트의 데이터 이름"></app-header>


**props.html**
```JS

    var appHeader = {
            template: '<h1>header</h1>',
            props: ['propsdata']                        // 하위 컴포넌트의 속성에 정의
    }

// 상위 컴포넌트 템플릿
    <div id="app">
        <app-header v-bind:propsdata="message"></app-header> // 하위 컴포넌트 태그에 v-bind 속성 정의
    </div>
 ```

##   :green_book: event emit
> 다른 컴포넌트에게 이벤트를 전달하기 위해 사용

###  ✍ event 속성 코드 형식 
- ```하위 --> 상위 ``` :  <app-header v-on: 하위 컴포넌트에서 발생한 이벤트 이름 = "상위 컴포넌트의 메서드 이름"></app-header>

	```JavaScript
	 this.$emit('이벤트명');
	```
- 상위 컴포넌트의 템플릿 
	```
    JavaScript
	<div id="app">
        <app-header v-on:이벤트명="상위 컴포넌트의 실행할 메서드 명 또는 연산">
        </app-header>
    </div> 
    ```
 <hr/>
 
 :speech_balloon: **참고**


1) $emit() 호출하면 정의된 이벤트가 발생됨
2) 호출한 이벤트를 v-on 속성으로 받음.(호출될 상위 메서드명 지정)

---
##   :blue_book: 뷰 인스턴스에서의 this
- [this관련](https://www.w3schools.com/js/js_this.asp)
- [this관련2](https://medium.com/better-programming/understanding-the-this-keyword-in-javascript-cb76d4c7c5e8)