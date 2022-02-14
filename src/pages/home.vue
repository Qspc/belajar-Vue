<template>
  <q-page class="flex flex-center">
    <!-- dropdown data -->
    <q-card dark bordered class="bg-grey-9 my-card">
      <q-card-section>
        <div class="text-h4">To do List</div>
      </q-card-section>

      <q-separator dark inset />

      <q-card-section>
        <div class="row justify-center">
          <div class="col-12">
            <q-input v-model="todoTask" label="standard" style="color: white">
              <template v-slot:after>
                <q-btn
                  round
                  dense
                  flat
                  icon="send"
                  @click="addItem"
                /> </template
            ></q-input>
          </div>
        </div>
      </q-card-section>
      <q-card-section>
        <div
          class="row justify-center"
          v-for="(item, index) in todoList"
          :key="index"
        >
          <div class="col-8 q-py-md">
            {{ item.value }}
          </div>
          <div class="col-auto q-py-md">
            <q-btn round dense flat icon="done" @click="removeItem(index)" />
          </div>
        </div>
      </q-card-section>
    </q-card>
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
