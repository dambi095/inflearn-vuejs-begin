###### 참고 코드 파일 : [watch.html, computed.html, watch-vs-computed.html]

#### 1. watch
watch 안에 선언된 data 값이 변환될 때 마다 안에 선언한 메서드가 호출된다.

#### 2. watch 와 computed 의 차이..?
computed 같은 경우는 validation, 단순한 값에 대한 계산할 때 사용하는것이 좋고, watch 같은 경우는 매번 실행되는게 부담스러운 로직(데이터 요청)에 사용하는 것이 좋다. vue 공식문서에서는 computed 사용을 권장..!