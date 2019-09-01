<template>
  <div>
    <TodoList />
    <DeletedList />
    <DoneList />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import TodoList from "@/components/TodoList.vue";
import DeletedList from "@/components/DeletedList.vue";
import DoneList from "@/components/DoneList.vue";

@Component({
  components: {
    TodoList,
    DeletedList,
    DoneList
  }
})
export default class Todo extends Vue {}
</script>
