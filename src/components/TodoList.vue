<template>
  <div>
    Todo list
    <TodoItem></TodoItem>
    <ul class="todoItems">
      <li v-for="item in 5" :key="item">
        <TodoItem></TodoItem>
      </li>
    </ul>
  </div>
</template>

<script>
import { Component, Vue } from 'vue-property-decorator';
import TodoItem from '@/components/TodoItem.vue';

@Component({
  components: {
    TodoItem,
  },
})
export default class TodoList extends Vue {}
</script>

<style>
</style>
