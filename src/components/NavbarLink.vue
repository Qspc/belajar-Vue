<template>
  <q-toolbar>
    <q-btn
      flat
      dense
      round
      icon="menu"
      aria-label="Menu"
      @click="toggleLeftDrawer"
    />

    <q-toolbar-title> Quasar hihi </q-toolbar-title>

    <div>Quasar v{{ $q.version }}</div>
  </q-toolbar>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "NavbarLink",
  // setup() {
  //   const leftDrawerOpen = ref(true);

  //   return {
  //     toggleLeftDrawer() {
  //       leftDrawerOpen.value = !leftDrawerOpen.value;
  //     },
  //   };
  // },
});
</script>
