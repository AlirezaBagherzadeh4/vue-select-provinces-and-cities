<template>
  <Select> </Select>
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
body {
  margin: 0 !important;
  padding: 0 !important;
}
#app {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #bee3db;
  color: #555b6e;
}
</style>
