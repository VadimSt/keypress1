<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <KeyPress key-event="keypress" :key-code="97" @success="onKeyPressZero" @any="onAnyKey"/>
</template>

<script>
import {defineAsyncComponent} from 'vue'
import {keys} from 'keycodes-map'
// import KeyPress from 'vue3-keypress'

const KeyPress = defineAsyncComponent(()=>import('vue3-keypress'))

export default {
  components:{
    KeyPress
  },
  data(){
    return {
    multiple:[
      {
        keyCode:'a',
        preventDefault: true
      }
    ],
    keys
  }},
  methods:{
    onKeyPressZero(){
      console.log('Zero')
    },
    onAnyKey(e){
      console.log(e.event.key)
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
</style>
