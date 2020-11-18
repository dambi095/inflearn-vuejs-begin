<template>
    <div id="app">
       <app-header v-bind:propsdata="str" v-on:renew="renewStr"></app-header>
    </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'; //appHeader 불러오기

export default {
  data: function(){
    return {
      str: 'props -> header'
    }
  },
  components: {
    'app-header' : AppHeader
  },
  methods: {
    renewStr: function() {
      this.str = 'hi'
    }
  }
}
</script>

<style>

</style>