<template>
  <div id="app">
  
  <h1>{{title}}</h1>
  
  <br>
  <h3>All task</h3>
  <task-list />

  <br>
  <h3>Completed task</h3>
  <task-list/>

  <br>
  <h3>Incompleted task</h3>
  <task-list/>
  
  </div>
</template>

<script>
import TaskList from "./Task";

export default {
  name: "app",
  data() {
    return {
      title: "Welcome to TaskPad in Vue.js"
    };
  },
  components: {
    "task-list": TaskList
  }
};
</script>

<style>
</style>
