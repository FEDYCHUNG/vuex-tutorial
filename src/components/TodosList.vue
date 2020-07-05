<style>
</style>

<template>
  <div>
    <todo v-for="(todo, index) in todos" :key="index" :todo="todo" />
  </div>
</template>

<script>
import todo from "./Todo";

export default {
  components: {
    todo
  },
  computed: {
    todos() {
      return this.$store.state.todos;
    }
  }
};
</script>