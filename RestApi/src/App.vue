<script>
// import HelloWorld from './components/HelloWorld.vue'
// import TheWelcome from './components/TheWelcome.vue'

import axios from "axios";

export default {
  name: 'App',
  data(){
    return{
      countries:[]
      // countrie: {}
    }
  },
  created(){
    axios.get('https://restcountries.com/v2/all').then((res)=>{
      // console.log(res.data); 
      this.countries = res.data
    })
    // axios.get('https://restcountries.com/v2/all/4/').then((res)=>{
    //   this.countries =res.data
    // })
  }
}

</script>

<template>
  <div id="app">
    countrie:{{ countries.name }}
    <hr>
    <ul>
      <li v-for="countrie in countries" :key="countrie.id">
        <h2>name:{{ countrie.name }}</h2>
        <h3>image:{{ countrie.flag }}</h3>
        <h4>population:{{ countrie.population }}</h4>
        <h5>region:{{ countrie.region }}</h5>
        <h6>capital:{{ countrie.capital }}</h6>
      </li>
    </ul>
  </div>
</template>

<style>


  
</style>
