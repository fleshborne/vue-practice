<template>
  <div>
    <TodoList :todos="todos" />
    <TodoForm @add-todo="addTodo" />
    <!-- conditionally render with v-if -->
    <!-- <p v-if="showMesage">{{ message.toUpperCase() }}</p> -->
    <!-- <label>Message:</label> -->
    <!-- v-model is the same hooking components together  -->
    <!-- <input type="text" v-model="message" /> -->

    <!--
    ':' means evalute, if no colon, it's treated as a string 
    <img :src="src" /> -->
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue';
import TodoForm from './components/TodoForm.vue';
export default {
  name: 'App',
  components: {
    TodoList,
    TodoForm,
  },
  data: function() {
    return {
      // message: 'this is the message that will be displayed.',
      todos: ['Clean', 'Do the Thing', 'Eat', 'Sleep'],
      // showMesage: true,
      // src: 'http://placekitten.com/600/400',
      newTodo: '',
    };
  },
  methods: {
    addTodo: function(newTodo) {
      // get the input from the user
      this.todos.push(newTodo);
      // and add the new item to the todo list

      // after you push a new todo, this will clear the input field
    },
  },
};
</script>

<style></style>
// wow new vue stuff
