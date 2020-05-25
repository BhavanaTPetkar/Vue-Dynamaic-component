<template>
  <div id="app">
    <button style ="background-color: green" @click="selectedComponent = 'appGreen'">Green</button>
    <button style ="background-color: red" @click="selectedComponent = 'appRed'">Red</button>
    <button style ="background-color: blue"  @click="selectedComponent = 'appBlue'">Blue</button>
    <component :is= "selectedComponent"><p>This is content</p></component>
  </div>
</template>

<script>
import Blue from "./components/Blue.vue";
import Green from "./components/Green.vue";
import Red from "./components/Red.vue";

export default {
  name: "App",
  components: {
    appGreen: Green,
    appRed: Red,
    appBlue: Blue
  },
  data: function() {
    return {
      selectedComponent: "appGreen"
    };
  }
};
</script>

<style scoped>
button {
  border: 1px solid white;
  padding: 15px;
  margin: 15px;
  border-radius: 8px;
}
</style>
