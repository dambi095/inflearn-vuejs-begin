<template>
  <form v-on:submit.prevent="submitForm"> //submit 이라는 이벤트를 받아서 메소드 실행
    <div>
      <label for="username">id: </label>
      <input v-model="username" id="username" type="text"> <!-- 입력한 데이터가 적용-->
    </div>
    <div>
      <label for="password">pw: </label>
      <input v-model="password" id="password" type="password">
    </div>
    <button type="submit">login</button> <!-- submit : 새로고침이되버림 -->
  </form>
</template>

<script>
import axios from 'axios';

export default {
  data: function() {
    return {
      // 컴포넌트간의 데이터가 공유되지 않게!
      username: '',
      password: ''
    }
  },
  methods: {
    submitForm: function() {
      //event.preventDefault(); // 폼의 새로고침을 막아줌 (js 방식)
      console.log(this.username + this.password);
      var url = 'https://jsonplaceholder.typicode.com/users';
      var data = {
        username: this.username, 
        password: this.password
      }
      axios.post(url, data) //데이터 전송을 위한 라이브러리(axios) post: 데이터를 저장하거나 조작할때
        .then(function (response){
          console.log(response);
        })
        .catch(function(error){
          console.log(error);
        });
    }
  }
}
</script>

<style>

</style>