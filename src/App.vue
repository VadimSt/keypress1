<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <KeyPress
    key-event="keyup"
    :multiple-keys="multipleKeys"
    @success="onSuccess"
    @any="onAnyKey"
  />
</template>

<script>
import { defineAsyncComponent } from "vue";
import { keys } from "keycodes-map";
import {multipleKeys} from './keyPress'

const KeyPress = defineAsyncComponent(() => import("vue3-keypress"));

export default {
  components: {
    KeyPress,
  },
  data() {
    return {
      eventSuccess: {
        0: this.onKeyPressDigit0,
        1: this.onKeyPressDigit1,
        2: this.onKeyPressDigit2,
        3: this.onKeyPressDigit3,
        4: this.onKeyPressDigit4,
        5: this.onKeyPressDigit5,
        6: this.onKeyPressDigit6,
        7: this.onKeyPressDigit7,
        8: this.onKeyPressDigit8,
        9: this.onKeyPressDigit9,
        '+': this.onKeyPressAdd,
        '-': this.onKeyPressSub,
        '=': this.onKeyPressCalc,
        '/': this.onKeyPressDivide,
        '*': this.onKeyPressMulty,
        'Delete': this.onKeyPressDel,
        'Enter': this.onKeyPressCalc,
        'Escape': this.onKeyPressEscape,
        'Backspace': this.onKeyPressBackspace,
      },
      multipleKeys,
    }
  },
  methods: {
    isKeyReserved(keySome){
      return Object.keys(this.eventSuccess).some(key=>key==keySome)},

    onKeyPressDigit1() {
      console.log("One");
    },
    onKeyPressDigit2() {
      console.log("Two");
    },
    onKeyPressDigit3() {
      console.log("Three");
    },
    onKeyPressDigit4() {
      console.log("Four");
    },
    onKeyPressDigit5() {
      console.log("Five");
    },
    onKeyPressDigit6() {
      console.log("Six");
    },
    onKeyPressDigit7() {
      console.log("Seven");
    },
    onKeyPressDigit8() {
      console.log("Eight");
    },
    onKeyPressDigit9() {
      console.log("Nine");
    },
    onKeyPressDigit0() {
      console.log("Zero");
    },
    onKeyPressCalc() {
      console.log("Calc");
    },
    onKeyPressDivide() {
      console.log("Divide");
    },
    onKeyPressMulty() {
      console.log("Multy");
    },
    onKeyPressAdd() {
      console.log("Add");
    },
    onKeyPressSub() {
      console.log("Sub");
    },
    onKeyPressDel() {
      console.log("Delete");
    },
    onKeyPressEscape() {
      console.log("Escape");
    },
    onSuccess(res) {
      let key = res.event.key
      if (!this.isKeyReserved(key)) {return console.log("Клавиша не зарезервирована")}
      this.eventSuccess[key]()
    },
    onAnyKey(e) {
      // console.log(e.event.key);
    },
  },
};
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
