<template>
  <div>
    <!-- evet.preventDefault() 와 같이 새로고침을 막아줄 수 있다 -->
    <form @submit.prevent="submitForm">
      <div>
        <label for="username">id:</label>
        <input type="text" id='username' v-model="username">
      </div>
      <div>
        <label for="password">pw:</label>
        <input id='password' type="password" v-model="password"/>
      </div>
      <button type="submit">login</button>
    </form>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data: function() {
    return {
      username: '',
      password: '',
    }
  },
  methods: {
    submitForm: function() {
      // event.preventDefault();
      console.log(this.username, this.password);
      const url = 'https://jsonplaceholder.typicode.com/users';
      const data = {
        username: this.username,
        password: this.password
      }
      axios.post(url, data)
      .then((response) => {
        console.log(response); 
      })
      .catch((error) => {
        console.log(error);
        
      });
    }
  }
}
</script>

<style>

</style>