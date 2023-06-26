<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <router-view/>

  <Card/>

<h1>Products</h1>

<p>{{'shoes'}}</p>

</template>




<script>

import Card from '../src/components/Card.vue';
  export default {
    components:{
      Card
    }
  
  }

  export   {
data(){
  return{
    shoes:[]
  }
},
  mounted(){
    fetch('https://jason-barron07.github.io/Vue-prod/vue-products/data/db.json')
    .then(res => res.json())
    .then(data => this.shoes = data)
    .catch(err => console.log(this.shoes))
  }
}

</script>

//vuex , redirectives, acious

<style>

*{

  margin:0;
  padding:0;
  box-sizing: border-box;

}

body{

  height: 100vh;

}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}


</style>