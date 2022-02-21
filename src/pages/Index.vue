<template>
  <q-page class="flex flex-center">
    <header :nama="dodi">
      <img src="react.png" alt="" style="width: 100px" />
      <h1>{{ pesan }}</h1>
      <h1>{{ nama }}</h1>
    </header>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "PageIndex",
  props: ["nama"],
  data() {
    return {
      pesan: "hallo dunia!",
    };
  },
  methods: {},
});

// Vue.component("header-component", {
//   props: ["nama"],
//   template: `
//         <header>
//             <img src="react.png" alt="" style="width: 100px" />
//             <h1>{{ pesan + ' ' + nama }}</h1>
//         </header>`,
//   data: function () {
//     return {
//       pesan: "hallo dunia!",
//     };
//   },
// });
</script>

<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 450px
</style>
