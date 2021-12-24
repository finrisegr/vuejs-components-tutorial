<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
    <simple-component :fname="name" :mname="middlename" />
    <simple-component
      :fname="surname"
      :mname="middlename"
      @clickFromChildComponent="handleClickInParent"
    />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import SimpleComponent from "./components/SimpleComponent.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    SimpleComponent,
  },
  methods: {
    handleClickInParent(val1, val2) {
      alert(val1 + " " + val2);
    },
  },
  data() {
    return {
      name: "Aniket",
      surname: "Aryamane",
      middlename: "Arun",
    };
  },
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
