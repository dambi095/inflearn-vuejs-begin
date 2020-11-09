#### 1. 뷰 컴포넌트 
&nbsp; 화면에 따라서 영역별로 코드를 관리한다. 컴포넌트를 구분했을 때 컴포넌트 간의 관계가 생긴다. </br>
&nbsp; 관계가 생긴다는 것은 컴포넌트간의 규칙이 생긴다는  것이다. 이러한 컴포넌트간의 규칙으로 인하여 컴포넌트간의 데이터의 흐름을 추적할 수 있다.

#### 2. 컴포넌트간의 데이터를 전달법
props : 상위에서 하위로는 데이터를 내려줌 </br>
event emit : 하위에서 상위로는 이벤트를 올려준다.

#### 3. v-on:, v-bind:
v-on 은 @ 로 v-bind는 : 로 축약이 가능하다!

#### 4. 뷰 인스턴스에서의 this ? 
```
let obj = {
    num: 10,
    getNumber: function() {
        // obj의 num 값을 가져온다.
        console.log(this.num); 
    }
}
obj.getNumber() // 10 !
```

```
let Vue = {
    el: '',
    data: {
        num: 10,
    }
    methods: {
        getNumber: function() { 
            this.num
        }
    }
}
```
메서드 함수안에서 this 는 해당 data 안의 num 을 바라본다. Vue 내부의 동작에 의해 data 안에 선언한 num이 바깥 레벨로 빠져 나와진다. 때문에 this를 이용하여 접근이 가능하다. 

