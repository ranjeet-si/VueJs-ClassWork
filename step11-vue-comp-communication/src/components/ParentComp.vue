<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <input type="text" v-model="message">
    <ChildComp @changeTitle="changeTitlefromChild" :msg="message" ></ChildComp>
  </div>
</template>
 
<script>
import ChildComp from './ChildComp.vue';
 
export default {
  name: 'ParentComp',
  data(){
    return {
      message : "Message from Parent Component"
    }
  },
  methods : {
    changeTitlefromChild(val){
      this.message = val;
    }
  },
  props: {
    msg: String
  },
  components : {
    ChildComp
}
}
</script>
 
<style scoped>
</style>
 