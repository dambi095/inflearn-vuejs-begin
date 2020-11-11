Chap8,9. 템플릿 문법
===
  
뷰 템플릿 문법
---
뷰로 화면을 조작하는 방법, 데이터바인딩 + 디렉티브
  
데이터 바인딩 
---
- {{}} : 콧수염태그(Mustache Tag)
- 문자열등 데이터를 담아두고 화면에 연결할떄 쓰는 방법
  
디렉티브
---
- HTML의 기본 표준속성을 제외한 v-로 시작되는 속성들
- HTML 표준 속성을 Vue의 데이터로 관리할떄 사용
- v-if : 조건에 따라 해당 태그의 활성화 여부를 결정(DOM 자체의 생성여부)
- v-show : 조건에 따라 해당 태그의 display 여부를 결정
- v-model : v-bind와 v-on의 기능의 조합으로, 매번 사용자가 일일이 v-bind와 v-on 속성을 다 지정해 주지 않아도  
            좀 더 편하게 개발할 수 있게 고안된 문법

Computed vs Watch
---
watch(감시자)
---
- 특정 데이터의 변경에 따라 수행할 행동을 정의
- 무거운 Logic 특정 경우에만 수행할때 사용
- newValue와 oldValue를 가지고있음

computed 
---
- 빠르게 계산, Chacing 수행
- 단순한 값에 대한 계산, Validation에 사용됨
- Vue에서 Computed를 더 권장함

※ 참고자료  
  
---
[Watch vs Computed](https://vuejs.org/v2/guide/computed.html#ad)
