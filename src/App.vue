<template>
  <div class="all">
    <div class="pop">
      <button @click="popup=true;a=1" v-if="a==0 && popup==false">show</button>
      <popup v-show="popup" @close="popup=false;a=0"/>
    </div>
    <selman name="sahal"/>
    <selman name="azlam"/>
    <selman name="ashna"/>
  </div>
</template>

<script>
import selman from './components/selman.vue'
import popup from './components/popup.vue'

export default {
  name: "App",
  components:{
    selman,
    popup,
  },
  data(){
    return{
      popup: false,
      a: 0
      
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
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
.pop{
  background-color: blueviolet;
  text-align:center;
  margin-left: auto;
  margin-right: auto;

}


</style>
