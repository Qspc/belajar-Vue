<template>
  <q-page class="flex flex-center">
    <div class="q-pa-md row justify-center">
      <div style="width: 100%; width: 400px">
        <q-chat-message name="me" :text="['aserunt quibusdam']" sent />
        <q-chat-message class="q-mr-xl" name="Jane" :text="['Lorem ipsum,']" />
        <q-chat-message name="me" :text="['arum eni quibusdam']" sent />
        <q-chat-message name="me" :text="['arum t quibusdam']" sent />
      </div>
    </div>
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
