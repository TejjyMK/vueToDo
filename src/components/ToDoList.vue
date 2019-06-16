<template lang="pug">
    .holder 
        h1 Tejj's To Do List
        input.todo-input(type="text", placeholder='What needs to be done' v-model='newTodo' @keyup.enter='addtoDo') 
        | To Do List goes here
        .todo-item(v-for="todo in todos", :key='todo.id')
           | {{todo.title}}
   
</template>

<script>
export default {
  name: "ToDoList",
  data() {
    return {
      newToDo: "",
      idForTodo: 3,
      todos: [
        {
          id: 1,
          title: "Finish Vue",
          completed: false
        },
        {
          id: 2,
          title: "Make breakfast",
          completed: false
        }
      ]
    };
  },
  methods: {
    addtoDo() {
      this.todos.push({
        id: this.idForTodo,
        title: this.newTodo,
        completed: false
      });

      this.newTodo = "";
      this.idForTodo++;
    }
  }
};
</script>

<style lang="sass">

  .holder
    text-align: left

  .holder h1
    text-align: center

  .todo-input
    width: 100%
    padding: 10px 18px
    font-size: 18px
    margin-bottom: 20px

    &:focus
        outline: 0 
        outline-color: gold
        
</style>
