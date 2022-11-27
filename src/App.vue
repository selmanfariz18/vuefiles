<template>
  <div  id="app">
    <div>hello {{name}}</div>
    <h2 v-if="num==0">Is it working</h2>
    <h2 v-else-if="num>0">The num is +ve</h2>
    <h2 v-else-if="num<0">The num is -ve</h2>
    <h2 v-else>Its not working</h2>
    <p v-show="see">v-show used</p>
    <p v-for="(name,index) in names" :key="name">{{index+1}}:{{name}}</p>
    <h2 v-for="name in fullnames" :key="name.first">{{name.first}} {{name.last}}</h2>
  </div>
</template>

<script>


export default {
  name: "App",
  data(){
    return{
      name:"selman",
      channel:"github",
      num:0,
      see:false,
      names:['selman','sahal','yasee'],
      fullnames:[{first:'Selmanul',last:'Farizy'},
                {first:'Sahal',last:'Shamsu'},
                {first:'Muhammed',last:'Yaseen'}]
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
