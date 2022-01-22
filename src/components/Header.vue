<template>
  <header>
    <h1>{{ title }}</h1>
    <Button
      v-show="homePage"
      @toggle-add-task="$emit('toggle-add-task')"
      :text="showAddTask ? 'Close Task' : 'Add Task'"
      :color="showAddTask ? 'red' : 'green'"
    />
  </header>
</template>

<script>
import Button from "./Button.vue";
export default {
  name: "header",
  props: { title: String, showAddTask: Boolean },
  components: { Button },
  computed: {
    homePage() {
      if (this.$route.path === '/') {
        return true;
      } else {
        return false;
      }
    },
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>