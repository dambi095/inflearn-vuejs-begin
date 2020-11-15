> #   컴포넌트 통신 방법 - 응용

 ##  :closed_book: 같은 컴포넌트 레벨 간의 통신 방법

![component](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FdcTicl%2FbtqxMsxoaCj%2FXDflkn69PF1ukmEKyXPGuK%2Fimg.png)
같은 레벨일 경우 바로 데이터 전달이 불가능하기 때문에
 -> **상위 컴포넌트에 값을 올린후 상위 컴포넌트에서 값을 내려 받아야 함**
		``` appContent --(event)--> Root --(props)--> appHeader```

### ✍ 같은 레벨간의 통신 방법
```
- 상위 컴포넌트로 넘길 데이터를 올림(event) *상위 컴포넌트는 값을 받기 위해 data가 선언되어 있어야 함
- 상위 컴포넌트의 값을 내려받음(props) 
 ```