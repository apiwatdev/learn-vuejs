<template>
  <header>
    <h1>{{ title }}</h1>
    <Button @click="onClick()" text="Add Task" color="green"/>
  </header>
</template>

<script>
import Button from './Button.vue';
export default {
  components: { Button },
  name: "Header",
  props: {
    title: String,
  },
  methods: {
    onClick(){
      console.log("click")
    }
  }

};
</script>

<style scope>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>