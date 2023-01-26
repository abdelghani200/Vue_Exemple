<script>
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'

import axios from "axios";

export default {
  name: 'App',
  data(){
    return{

    }
  },
  created(){
    axios.get('https://restcountries.com/v2/all').then((res)=>{
      console.log(res.data); 
    })
  }
}

</script>

<template>
  <div id="app">

  </div>
</template>

<style>


  
</style>
