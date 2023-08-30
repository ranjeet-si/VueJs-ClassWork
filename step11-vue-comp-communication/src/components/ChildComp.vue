<template>
  <div class="box">
    <h1>Child Component</h1>
    <h2>{{ msg }}</h2>
    <button @click="$emit('changeTitle', 'There\'s no turning back')">
      Set message on parent to There's no turning back
    </button>
  </div>
</template>

<script>
export default {
  name: "ChildComp",
  emits: ["changeTitle"],
  props: {
    msg: String,
  },
};
</script>

<style scoped>
.box {
  border: 2px solid grey;
  padding: 10px;
  margin: 10px;
}
.box h2 {
  color: crimson;
}
</style>
