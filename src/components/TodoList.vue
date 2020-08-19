<template>
  <div>
    <h1>{{ todosCount }} Todo Items</h1>
    <ul>
      <li v-for="todo in todos" :key="todo">
        {{ todo }}
      </li>

      <!-- @ = shortcut for events! -->
    </ul>
  </div>
</template>

<script>
export default {
  name: 'TodoList',
  props: ['todos'],
  computed: {
    todosCount: function() {
      return this.todos.length;
    },
  },
  //   if you were to pull this todo list from an api, below is how you'd do it.
  //   created: function() {
  //     axios.get('/todos').then((res) => {
  //       this.todos = res.data;
  //     });
  //   },
};
</script>

<style></style>
