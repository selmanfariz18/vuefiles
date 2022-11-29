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
    <h2>sum:{{add(5,5,5)}}</h2>
    <button v-on:click="name='Fariz'">click</button>
    <h1>{{count}}</h1>
    <div>
      <button v-on:click="count+=1">Add</button>
      <button v-on:click="count-=1">substract</button>
      <button v-on:click="count=0">reset</button>
    </div>
  </div>
</template>

<script>


export default {
  name: "App",
  data(){
    return{
      name:"selman",
      channel:"github",
      count:0,
      num:0,
      see:false,
      names:['selman','sahal','yasee'],
      fullnames:[{first:'Selmanul',last:'Farizy'},
                {first:'Sahal',last:'Shamsu'},
                {first:'Muhammed',last:'Yaseen'}]
    }
  },
  methods: {
    add(a,b,c){
      return a+b+c
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
