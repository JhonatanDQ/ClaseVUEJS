<script setup>

import { ref } from 'vue';

const mensaje = "mundo"
const val1 = 0
const val2 = ref(0)

</script>

    <template>
      hola {{mensaje}}.
      <div id="wrapper">
      <svg id="icon" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
  <path stroke-linecap="round" stroke-linejoin="round" d="M17.982 18.725A7.488 7.488 0 0012 15.75a7.488 7.488 0 00-5.982 2.975m11.963 0a9 9 0 10-11.963 0m11.963 0A8.966 8.966 0 0112 21a8.966 8.966 0 01-5.982-2.275M15 9.75a3 3 0 11-6 0 3 3 0 016 0z" />
</svg>
<div id="globito">
{{ val2 }}
</div>
</div>

<button id="btn1" v-on:click="val2 += 1">+</button>
      <button id="btn2" v-on:click="val2 -= 1">-</button>

     <span id="btn">-</span>
     <span id="btn">+</span>


    </template>

<style scoped>
#icon {
  width: 42px;
  height: 42px;
}

#btn1{
  width: 52px;
  height: 22px;
  text-align: center;
  font-weight: bold;
  background-color: aqua;
  border-radius: 15%;
}

#btn2{
  width: 20px;
  height: 20px;
  text-align: center;
  font-weight: bold;
  background-color: lime;
  border-radius: 15%;
}

#globito{
background-color: red;
font-weight: bold;
text-align: center;
height: 24px;
width: 24px;
border-radius: 100%;
cursor: default;
position: absolute;
top:-12px;
right:-12px
}

#wrapper{
  width: 44px;
   display: inline-block;
  position: relative;
}

#btn {
  display: inline-block;
  margin:4px;
  position: relative;
  background-color: gray;
  color: white;
  width:32px;
  height: 32px;
  text-align: center;
  border-radius: 6%;
}
</style>
