###### 참고 폴더 : vue-cli

#### 1. Vue CLI (Command Line Interface)
```
명령어를 통한 특정 액션을 수행하는 도구를 뜻한다. 
```

#### 2. Vue CLI 를 시작 전 버전을 확인하자
```
node -v : 노드는 10 이상이여야 한다. 
```

#### 3. Vue CLI 를 시작해보자!
```
npm install -g @vue/cli 또는 yarn global add @vue/cli
```

#### 4. Vue 프로젝트를 생성하자
```
[Vue CLI 2.x]
vue init '프로젝트 템플릿 유형' '프로젝트 폴더 위치'
vue init webpack-simple '프로젝트 폴더 위치'

[Vue CLI 3.x] 
vue create '프로젝트 폴더 위치'

// 프로젝트 생성~
vue create vue-cli

// 프로젝트로 이동 
cd '생성한 프로젝트 명'

// 서버 실행!
npm run serve
```

#### 5. template 생성 단축키
vu + tab 클릭 시 template 틀이 잡힌다.