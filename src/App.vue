<template>
  <div id="app">
    <!--<compo-a :name="myName" :age="age" :person="person"/>-->
    <img src="https://via.placeholder.com/350x150" v-if="visible"
    :style="{opacity: (transluscence) ? 0.2 : 1, background: 'pink'}">
    <hr/>

    <my-button
    v-on:my-button-click="visible = false"
    :options="{color: 'red', size: 'big', text: 'Hide Me'}"/>
    <hr/>
    <my-button
    v-on:my-button-click="visible = true"
    :options="{color: 'blue', size: 'small', text: 'UnHide Me'}"/>
    <hr/>
    <my-button
    v-on:my-button-mouseover="transluscence = true"
    v-on:my-button-mouseout="transluscence = false"
    :options="{color: 'green', size: 'big', text: 'Translucense on Hover'}"/>
  </div>
</template>

<script>
import CompoA from "./components/CompoA";
import MyButton from "./components/MyButton";

export default {
  name: "App",
  components: {
    CompoA,
    MyButton
  },
  data() {
    return {
      visible: true,
      transluscence: false,
      myName: "Saikat",
      age: 30,
      person: {
        name: "Debdut",
        age: 20,
        phone: 2020,
        friends: ["1", "2", "2", "5"]
      }
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
