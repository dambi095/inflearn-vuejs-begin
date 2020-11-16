  #  템플릿문법 - 실전
  > 뷰로 화면을 조작하는 방법
  
   ##  :closed_book: computed
   > 이미 존재하는 값을 이용하여 새로운 값을 생성 즉, 기존 데이터의 값에 따라 변화하는 값을 정의할 때 사용

- 데이터 속성 값이 변화에 따라 자동으로 다시 연산
- 연산의 결과값을 미리 저장하고 있다가 필요할 때 불러올 수 있음- 

## :ledger: watch
> 데이터 변화를 감지하여 자동으로 특정 **로직**을 수행 함
> 데이터 호출과 같이 시간이 상대적으로 더 많이 소모되는 비동기 처리에 적합

 :speech_balloon: **추가**
**v-bind:class="{ warning: isError }"**
- [공식문서 computed vs watch](https://vuejs.org/v2/guide/computed.html#ad )