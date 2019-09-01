<template>
  <div class="container">
    <TodoList class="todoList" />
    <DeletedList class="deletedList"/>
    <DoneList class="doneList"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import TodoList from '@/components/TodoList.vue';
import DeletedList from '@/components/DeletedList.vue';
import DoneList from '@/components/DoneList.vue';

@Component({
  components: {
    TodoList,
    DeletedList,
    DoneList,
  },
})
export default class Todo extends Vue {}
</script>

<style lang="scss">
@media screen {
  
}

.container {
  display: grid;
  grid-template-areas: "todoList doneList"
                        "todoList deletedList"
}

.todoList {
  grid-area: todoList;
  border: solid 1px green;
}

.deletedList {
  grid-area: deletedList;
  border: solid 1px blue;
}

.doneList {
  grid-area: doneList;
  border: solid 1px red;
}
</style>
