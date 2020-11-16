 #  HTTP 통신 라이브러리 - axios
   ##  :closed_book: Axios - Promise 기반의 API 형식
   > promise: 서버에 데이터를 요청하여 받아오는 동작과 같은 비동기 로직 처리에 유용한 자바스크립트 객체로 데이터를 요청하고 받아올 때까지 기다렸다가 화면에 나타나는 로직을 실행해야 할 때 주로 사용

	**axios 사용** : ``` <script src="https://unpkg.com/_axios_/dist/_axios_.min.js"></script> ```

```js
	// ex
	axios.get('https://jsonplaceholder.typicode.com/users/')
		.then(function(response)  {  /* 성공일 때 */
			console.log(response);
			this.users  =  response.data;
		})
		.catch(function(error){  /* 실패일 때*/
		})
	..
```

**get** : ``` axios.get('URL주소').then(정상일때).catch(실패일때) ```
**post**  : ```axios.post('URL주소').then().catch()```
```axios({옵션 속성})```


   - [jsonplaceholder](https://jsonplaceholder.typicode.com/) : backend server가 없을 때 임시 가상 데이터를 만들어 api 테스트를 할 수 있음
   - [자바스크립트동작원리](https://joshua1988.github.io/web-development/translation/javascript/how-js-works-inside-engine/)
   
   
   ##  :ledger: HTTP 통신구조 
  ![클라이언트와 서버와의 HTTP 통신구조](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FZZwyG%2FbtqxOIGoKkh%2FoH6OKELLMTzAktKYq3NUAK%2Fimg.png)