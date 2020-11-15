Vue CLI
===
  
  
Vue CLI 2.x(기존 CLI)
---
vue init '프로젝트 템플릿 유형'  '프로젝트 폴더 위치'  
vue init webpack-simple  '프로젝트 폴더 위치'  
  
Vue CLI 3.x(최신 CLI)
---
vue create '프로젝트 폴더 위치'  
템플릿 유형이 사라진 이유 : Vue CLI는 플러그인 기반  

vue create vue-cli 명령어 오류 발생시  
-> vue.cmd create vue-cli
  
※ 프로젝트명을 카멜식(ex:applePie)으로 입력할 경우 에러 발생. 반드시 케밥식으로 작성  
  
public > index.html의
app div에 webpack을 통해 주입됨  
[WebPack 정의](https://jeonghwan-kim.github.io/series/2019/12/10/frontend-dev-env-webpack-basic.html)

```
싱글파일 컴포넌트  
HTML / JAVASCRIPT / CSS로 화면의 영역을 나눠 한파일에서 관리
```

CLI의 .vue는 컴포넌트를 재사용 할 확률이 높으므로 data : 객체가 아닌
 data : fuction(){
	return{
	}
}
형태로 새객체를 반환해줘야함
