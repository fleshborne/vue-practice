<template>
  <div>
    <form @submit.prevent="addTodo">
      <input type="text" v-model="newTodo" />
      <button>+ Add Todo</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'TodoForm',
  //   maintain state with code below
  data: function() {
    return {
      newTodo: '',
    };
  },
  methods: {
    addTodo: function() {
      // complex function allowing for creation of event
      // takes 2 arguments
      // name of event, use kebab case
      // data
      this.$emit('add-todo', this.newTodo);
      this.newTodo = '';
    },
  },
};
</script>

<style scoped></style>
