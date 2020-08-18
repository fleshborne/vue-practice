<template>
  <div>
    <!-- conditionally render with v-if -->
    <!-- <p v-if="showMesage">{{ message.toUpperCase() }}</p> -->
    <!-- <label>Message:</label> -->
    <!-- v-model is the same hooking components together  -->
    <!-- <input type="text" v-model="message" /> -->

    <ul>
      <li v-for="todo in todos" v-bind:key="todo">
        {{ todo }}
      </li>
      <input type="text" v-model="newTodo" />
      <button @click="addTodo">+ Add Todo</button>
      <!-- @ shortcut for events! -->
    </ul>
    <!--
    ':' means evalute, if no colon, it's treated as a string 
    <img :src="src" /> -->
  </div>
</template>

<script>
export default {
  name: 'App',
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
    addTodo: function() {
      // get the input from the user
      this.todos.push(this.newTodo);
      // and add the new item to the todo list

      // after you push a new todo, this will clear the input field
      this.newTodo = '';
    },
  },
};
</script>

<style></style>
// wow new vue stuff
