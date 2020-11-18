  #  Vue CLI
  >  명령어를 이요해 뷰 애플리케이션을 개발하기 위한 초기 프로젝트구조를 구성함.
  
   ##  :closed_book: CLI 설치
   [CLI](https://cli.vuejs.org/guide/installation.html)

- **CLI 설치**
	-    ``` npm install -g @vue/cli```
		- 2.x 버전 삭제후 3.x 버전 설치시
			- ```npm r -g vue-cli -> npm i -g @vue/cli ```

- **버전체크**
	- node -v :  10점대 이상
	- npm -v : 6점대 이상


- **Vue CLI 도구 설치시 문제점 해결방법**
	https://stackoverflow.com/questions/5926672/where-does-npm-install-packages

## :ledger:  프로젝트 생성 및 서버 실행

** 

**[Vue CLI 2.x]**
```vue init '프로젝트 템플릿 유형' '프로젝트 폴더 위치'```
```vue init webpack-simple' '프로젝트 폴더 위치'```

**[Vue CLI 3.x]**
```vue create '프로젝트 위치'```
``` vue create vue-cli```

**서버 실행**
```cd vue-cli```
```npm run serve```

##   :green_book: 
vu + [tab] : 싱글 파일 컴포넌트 기본 코드 자동완성!

```JS
<template>
	<!-- HTML 태그 내용 -->
</template>

<script>
  export  default {
	//Javascript	
  }
</script>

<style>
	/* CSS */
</style>
```

- **&lt;template> : 화면에 표시할 요소들을 정의하는 영역 (HTML + 뷰 데이터 바인딩)**
- **&lt;script>: 뷰 컴포넌트의 내용을 정의 (template, data, methods ...)**
-  **&lt;style>: 템플릿에 추가한 HTML 태그의 스타일을 정의**