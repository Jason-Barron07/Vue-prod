<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  
<router-view/>
<!-- 
<div v-for="shoe in shoes"> </div> -->

<h1>SHOE SIZE</h1>

<p>the shoe size is {{size}}</p>


</template>

<style>

</style>

<script>

// export default {

// data(){

//   return{

//     shoes:[]

//   }

// },

//   mounted(){

//     fetch('/data/db.json')
//     .then(res => res.json())
//     .then(data => this.shoes = data)
//   }

// }

export default {

  props:["size"]


}




</script>