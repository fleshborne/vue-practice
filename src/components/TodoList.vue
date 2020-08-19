<template>
  <div>
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
};
</script>

<style></style>
