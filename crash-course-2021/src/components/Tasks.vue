  
<template>
  <div>
    <div :key="task.id" v-for="task in tasks">
     <task @toggle-reminder="$emit('toggle-reminder',task.id)" @delete-task="$emit('delete-task',task.id)" :task="task" />   
    </div>
  </div>
</template>
<script>
import Task from './Task.vue';

export default {
  components: { Task },
  props: {
    tasks: Array,
  },
};
</script>

<style>
</style>