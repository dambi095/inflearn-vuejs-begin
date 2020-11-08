###### 참고 코드 파일 : instance.html

#### 1. 인스턴스 생성

```
new Vew() 를 사용하여 인스턴스를 생성할 수 있다. 

함수의 앞이 대문자이면 생성자 함수를 의미한다 
function Person(name, job) {
    this.name = name;
    this.job = job;
}

var dam = new Person('dambi', 'developer');
```

#### 2. 왜 Vue를 생성자 함수를 사용해서 이용할까?
 미리 정의된 속성, api를 정의해놓고 재사용하는 패턴을 사용하기 위해 new Vue() 로 선언한다.

```
function Vue() {
    this.logText = function () {
        console.log('hello');
    }
}

var vm = new Vue()

vm.logText(); // 'hello'
```

#### 3. Vue 인스턴스의 사용할 수 있는 속성

new Vue({ <br/>
&nbsp;    el: 인스터스가 그려지는 화면의 시작점 (HTML) , <br/>
&nbsp;    template: 화면에 표시할 요소 (HTML, CSS) , <br/>
&nbsp;    data: 뷰의 반응성과 반영된 데이터 속성 , <br/>
&nbsp;    methods: 화면의 동작과 이벤트 로직을 제어하는 메서드 , <br/>
&nbsp;    created: 뷰의 라이프 사이클과 관련된 속성 ,<br/>
&nbsp;    watch: data에서 정의한 속성이 변화했을 때 추가 동작을 수행할 수 있도록 정의하는 메서드 , <br/>
})