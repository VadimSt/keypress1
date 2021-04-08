<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <KeyPress
    key-event="keyup"
    :key-code="keys.num4"
    :multipleKeys="multiple"
    @success="onKeyPressZero"
    @any="onAnyKey"
  />
</template>

<script>
import { defineAsyncComponent } from "vue";
import { keys } from "keycodes-map";
// import KeyPress from 'vue3-keypress'



const KeyPress = defineAsyncComponent(() => import("vue3-keypress"));

const keysEvents = {
  keys.num1:,
}


export default {
  components: {
    KeyPress,
  },
  data() {
    return {
      multiple: [
        {
          keyCode: keys.num0,
          preventDefault: true,
        },
        {
          keyCode: keys.num1,
          preventDefault: true,
        },
        {
          keyCode: keys.num2,
          preventDefault: true,
        },
        {
          keyCode: keys.num3,
          preventDefault: true,
        },
        {
          keyCode: keys.num4,
          preventDefault: true,
        },
        {
          keyCode: keys.num5,
          preventDefault: true,
        },
        {
          keyCode: keys.num6,
          preventDefault: true,
        },
        {
          keyCode: keys.num7,
          preventDefault: true,
        },
        {
          keyCode: keys.num8,
          preventDefault: true,
        },
        {
          keyCode: keys.num9,
          preventDefault: true,
        },
        {
          keyCode: keys.numpad0,
          preventDefault: true,
        },
        {
          keyCode: keys.numpad1,
          preventDefault: true,
        },
        {
          keyCode: keys.numpad2,
          preventDefault: true,
        },
        {
          keyCode: keys.numpad3,
          preventDefault: true,
        },
        {
          keyCode: keys.numpad4,
          preventDefault: true,
        },
        {
          keyCode: keys.numpad5,
          preventDefault: true,
        },
        {
          keyCode: keys.numpad6,
          preventDefault: true,
        },
        {
          keyCode: keys.numpad7,
          preventDefault: true,
        },
        {
          keyCode: keys.numpad8,
          preventDefault: true,
        },
        {
          keyCode: keys.numpad9,
          preventDefault: true,
        },
        {
          keyCode: keys.numpadEqual,
          preventDefault: true,
        },
        {
          keyCode: keys.numpadDivide,
          preventDefault: true,
        },
        {
          keyCode: keys.numpadMultiply,
          preventDefault: true,
        },
        {
          keyCode: keys.numpadSubtract,
          preventDefault: true,
        },
        {
          keyCode: keys.numpadAdd,
          preventDefault: true,
        },
        {
          keyCode: keys.delete,
          preventDefault: true,
        },
        {
          keyCode: keys.num8,
          modifiers: ["shiftkey"],
          preventDefault: true,
        },
      ],
      keys,
    };
  },
  methods: {
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
    onAnyKey(e) {
      console.log(e.event.key);
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
