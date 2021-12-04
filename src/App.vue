<template>
  <Select />
</template>

<script>
import Select from "./components/Select.vue";

export default {
  name: "App",
  components: {
    Select,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Lalezar&display=swap");

* {
  font-family: "Lalezar", cursive;
}
body {
  margin: 0 !important;
  padding: 0 !important;
}
#app {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: flex-start;
  background-color: #bee3db;
  color: #555b6e;
  font-size: x-large;
  padding: 150px 0px;
}
</style>
