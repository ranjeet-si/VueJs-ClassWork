<template>
  <ParentComp msg="Welcome to Your Vue.js App"/>
</template>
 
<script>
import ParentComp from './components/ParentComp.vue'
 
export default {
  name: 'App',
  components: {
    ParentComp
  }
}
</script>
 
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>