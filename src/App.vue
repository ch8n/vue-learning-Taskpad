<template>
  <div id="app">
  
  <h1>{{title}}</h1>

  <h3>Add task</h3>
  <input type="text" v-modal="input_task" placeholder="task">
  <button @click="onclickAdd($event)">Add</button>
  
  
  <br>
  <h3>All task</h3>
  <div>
        <ol>
            <li v-for="(task,index) in tasks" :key="index">
                <p >::: {{task.name}} :::</p>
            </li>
        </ol>
  </div>

  <br>
  <h3>Completed task</h3>
  <div>
        <ol>
            <li v-for="(task,index) in completedTask" :key="index">
                <p >::: {{task.name}} :::</p>
            </li>
        </ol>
  </div>

  <br>
  <h3>Incompleted task</h3>
  <div>
        <ol>
            <li v-for="(task,index) in inCompletedTask" :key="index">
                <p >::: {{task.name}} :::</p>
            </li>
        </ol>
  </div>
  
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      title: "Welcome to TaskPad in Vue.js",
      tasks: [
        { name: "make header TaskPad", completed: true },
        { name: "make task component", completed: false },
        { name: "make list of sample task", completed: false },
        { name: "show list of task", completed: false },
        { name: "add checkbox against every task ", completed: false },
        {
          name: "click on checkbox change completed status ",
          completed: false
        },
        {
          name: "make 3 list all task ,completed and incompleted task ",
          completed: false
        },
        { name: "make field to take input of task ", completed: false },
        { name: "filter task according to task ", completed: false }
      ]
    };
  },
  methods: {
    onclickAdd(event) {
      alert(event);
    }
  },
  computed: {
    completedTask() {
      return this.tasks.filter(task => task.completed);
    },
    inCompletedTask() {
      return this.tasks.filter(task => !task.completed);
    }
  }
};
</script>

<style>
</style>
