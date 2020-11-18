<template>
    <div id="app">
        <img src="./assets/logo.png" alt="Vue logo">
        <HelloWorld msg="Welcome to Your Vue.js App" />
        <!-- 컴포넌트 명명법 종류 -->
        <!-- <hello-World></hello-World>
        <HelloWorld></HelloWorld>
        <HelloWorld/> -->
    </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
export default {
    // 인스턴스 옵션 속성 or 컴포넌트 옵션 속성
    name: 'app',
    components: {
        HelloWorld
    }
}
</script>

<style>
    /* CSS */
</style>