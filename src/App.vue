<template>
  <div>
    <p>{{ message.toUpperCase() }}</p>
    <label>Message:</label>
    <!-- v-model is the same hooking components together  -->
    <input type="text" v-model="message" />
    <table class="responsive-table" align="center">
      {{
        todos
      }}
    </table>
  </div>
</template>

<script>
export default {
  name: 'App',
  data: function() {
    return {
      message: 'this is the message that will be displayed.',
      todos: ['Clean', 'Do the Thing', 'Eat', 'Sleep'],
    };
  },
};
</script>

<style></style>
// wow new vue stuff
