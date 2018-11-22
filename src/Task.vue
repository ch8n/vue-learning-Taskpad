<template>
    <div>
        <ol>
            <li v-for="(task,index) in tasks" :key="index">
                <p>::: {{task.name}} ::: isComplted :::{{task.completed}} ::: <input type="checkbox" :checked="task.completed"></p>
            </li>
        </ol>
    </div>
</template>

<script>
export default {
  data() {
    return {
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
  }
};
</script>

<style>
</style>
