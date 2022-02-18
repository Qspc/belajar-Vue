<template>
  <q-page class="flex flex-center">
    <q-uploader
      url="http://localhost:4444/upload"
      color="teal"
      flat
      bordered
      style="max-width: 300px"
    />
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "PageIndex",

  data() {
    return {
      todoTask: "",
      todoList: [{ value: "Create an App" }, { value: "build a database" }],
    };
  },
  methods: {
    addItem() {
      this.todoList.push({ value: this.todoTask });
    },
    removeItem(index) {
      this.todoList.splice(index, 1);
    },
  },
});
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 450px
</style>
