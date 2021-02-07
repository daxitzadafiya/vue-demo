<template>
  <div id="app">
 <inputForm/>
 <mainGrid/>
 
  </div>
</template>

<script>

import inputForm from './components/inputForm'
// import innerDiv from './components/innerDiv'
import mainGrid from './components/mainGrid'
export default {
  name: 'App',
  components: {
 inputForm,
 mainGrid
  }
}
</script>

<style>
#app {
  margin-top: 20px;
}
</style>
