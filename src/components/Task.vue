<template>
  <div  @dblclick="$emit('toggle-reminder', task.id)"
    :class="[task.reminder ? 'reminder' : '', 'task']">
    <h3>{{ task.text }} <i @click="$emit('delete-task' ,task.id)" class="bi bi-trash"></i></h3>
    <p>{{ task.day }}</p>
  </div>
</template>
<script>
export default {
  name: "task",
  props: {
    task: Object,
  },
  methods: {
  },
};
</script>


<style lang="scss" scoped>
.bi-trash{
  color: red;
}
.task {
  background: #f4f4f4;
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
  h3 {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
}
.task.reminder {
  border-left: 5px solid green;
}
</style>