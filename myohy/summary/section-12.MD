 # [Project] 사용자 입력 폼 만들기
> ctrl + c : 서버 종료
> axios 설치 : npm i axios

##  :closed_book:  [Project] 00. 마크업
   
```js
<template>
	<form>
		<div>
			<label for="username">id: </label>
			<input id="username" type="text">
		</div>
		<div>
			<label for="password">pw: </label>
			<input id="password" type="password">
		</div>
		<button type="submit">login</button>  <!-- submit : 새로고침이되버림 -->
	</form>
</template>
```
##  :ledger:  [Project] 01. v-model 속성, submit 이벤트처리
```js
<template>
	<form  v-on:submit.prevent="submitForm"> //submit 이라는 이벤트를 받아서 메소드 실행
		<div>
			<label  for="username">id: </label>
			<input  v-model="username"  id="username"  type="text">  <!-- 입력한 데이터가 적용-->
		</div>
		<div>
			<label  for="password">pw: </label>
			<input  v-model="password"  id="password"  type="password">
		</div>
		<button  type="submit">login</button>  <!-- submit : 새로고침이되버림 -->
	</form>
</template>
```