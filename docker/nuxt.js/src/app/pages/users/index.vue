<template>
  <div>
    <input class="input" v-model="name">
    <button v-on:click="submit">send</button>
  </div>
</template>

<script>

const axios = require('axios');

export default {
  
  data() {
      return {
        name: ''
      }
    },
  methods:{
    submit: function() {
      axios.post('http://localhost:3000/users'), {
        name: this.name
      }
    }
  }

}
</script>

<style>
  
</style>