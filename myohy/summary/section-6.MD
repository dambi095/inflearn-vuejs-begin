  #   뷰 라우터
> 싱글 페이지 어플리케이션(SPA)을 구현할 때 상용하는 페이지 이동을 위한 라이브러리
 ##  :closed_book: 라우터 (CDN 방식)
```https://unpkg.com/vue-router/dist/vue-router.js](https://unpkg.com/vue-router/dist/vue-router.js```

## :ledger: 라우터 인스턴스 생성
```js
var router = new Router({ ... })

// 라우터를 사용하기 위해 뷰 인스턴스에 연결
new Vue({
	el: '#app',
	router: router // 라우터속성에 라우터 변수를 넣음
})
```
####  routes: 페이지의 라우팅 정보 , 어떤 url로 이동 했을때 어떤 페이지가 뿌려질지에 대한 정보
```js
routes: [
	{
		path: '/login', // 페이지의 url
		component: LoginComponent // 해당 url 에서 표시될 컴포넌트
	}, ...
]
```
```html
<div  id="app">
	<router-view></router-view>  <!-- 페이지 표시 태그 -->
	<div>
		<router-link  to="/login">Login으로 이동</router-link> 
		<router-link  to="/main">Main으로 이동</router-link>
	</div>
</div>

```
- ```<router-link to="URL">``` : 페이지 이동 태그, 화면 상 &lt;a&gt; 태그로 표시됨
- ```<router-view>``` : 페