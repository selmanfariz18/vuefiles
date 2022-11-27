<template>
  <div  id="app">
    <div>hello {{name}}</div>
    <h2 v-if="num==0">Is it working</h2>
    <h2 v-else>Its not working</h2>
  </div>
</template>

<script>


export default {
  name: "App",
  data(){
    return{
      name:"selman",
      channel:"github",
      num:0
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.all{
  text-align: center;
}
</style>
