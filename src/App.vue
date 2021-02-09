<template>
  <div id="app">
    <randaring />
  </div>
</template>

<script>
// import innerDiv from './components/innerDiv'
import randaring from "./components/randaring";

export default {
  name: "App",
  components: {
    randaring
  }
};
</script>

<style>
#app {
  margin-top: 20px;
}
</style>
