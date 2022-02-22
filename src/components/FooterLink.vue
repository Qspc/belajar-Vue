<template>
  <q-tabs>
    <q-tab name="mails" icon="mail" label="mails" />
    <q-tab name="alarms" icon="alarm" label="alarms" />
    <q-tab name="movies" icon="movie" label="movies" />
  </q-tabs>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "FooterLink",
});
</script>
