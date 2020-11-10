Chap7. HTTP 통신라이브러리 - axios
===

Vue resource
---
- 에반뉴는 Vue Resource를 공식라이브러리로 채택하지 않음
- pagekit 소유
- 예전 공식라이브러리이므로 legacy 코드로 존재할수 있으므로 참고할 상황 발생 가능

액시오스(axios)
---
- 뷰에서 권고하는 HTTP 통신 라이브러리
- Promise 기반의 HTTP 통신 라이브러리
- 다른 HTTP 통신 라이브러리들에 비해 문서화가 잘되어있고 API가 다양함
- [axios github](https://github.com/axios/axios)

```
※ Promise 
- 프로미스는 자바스크립트 비동기 처리에 사용되는 객체
- JavaScript 비동기처리 패턴
```

자바스크립트의 비동기 처리 패턴의 변천사
1. callback
2. promise
3. promise + generator
4. async + awit

[JSonplaceholder](https://jsonplaceholder.typicode.com)
- JavaScript API 요청 테스트 Site

```
※ axios.get() 호출 이후의 this와 이전의 this는 다름
- 호출전 this : 인스턴스 혹은 컴포넌트
- 호출후 this : 비동기처리를 후 실행 Context가 바뀌며 내용도 변경됨
```
※ 참고자료 
  
---
[자바스크립트 동작원리](https://joshua1988.github.io/web-development/translation/javascript/how-js-works-inside-engine)  
[구글 개발자도구 관련문서](https://developers.google.com/web/tools/chrome-devtools/)  
[Promise 정리](https://joshua1988.github.io/web-development/javascript/promise-for-beginners/)  
[async&await 정리](https://joshua1988.github.io/web-development/javascript/js-async-await/)  
