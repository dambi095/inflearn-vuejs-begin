<template>
  <!-- template root는 무조건 하나의 div 만을 가져야한다. -->
  <div>
    <app-header 
      :propsdata='str'
      @renew='renewStr'
    ></app-header>
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';

export default {
  data: function() {
    return {
      str: 'Header'
    }
  },
  components: {
    'app-header': AppHeader
  }, 
  methods: {
    renewStr: function() {
      this.str = 'hi';
    }
  }
}
</script>

<style>

</style>