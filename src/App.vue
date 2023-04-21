<template>
  <div class="container">
    <p>ເວີຊັ້ນ {{item[0].version}}</p>
    <router-view> </router-view>
    
  </div>
</template>

<script>
import axios from 'axios';
export default {
 data(){
  return{item:null}
 },

 mounted(){
  axios.get('https://script.google.com/macros/s/AKfycbzz-j83MrZomTfLaP-Sb0CsTdFcHGR-qTdPLb4L_GmnSrHrCbM0HUo1qS8G3B6YEiTrUQ/exec?action=getData').then((res) => {this.item=res.data})
 }
}
</script>
<style>
  
</style>