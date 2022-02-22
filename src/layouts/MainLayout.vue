<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <NavbarLink />
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header> My Project </q-item-label>
        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-footer elevated>
      <FooterLink />
    </q-footer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import EssentialLink from "components/EssentialLink.vue";
import FooterLink from "components/FooterLink.vue";
import NavbarLink from "components/NavbarLink.vue";

const linksList = [
  {
    title: "Hihi",
    caption: "quasar.dev",
    icon: "list",
    link: "/#/",
  },
  {
    title: "Home",
    caption: "github.com/quasarframework",
    icon: "home",
    link: "/#/home",
  },
  {
    title: "About",
    caption: "chat.quasar.dev",
    icon: "chat",
    link: "/#/about",
  },
  {
    title: "Forum",
    caption: "forum.quasar.dev",
    icon: "record_voice_over",
    link: "https://forum.quasar.dev",
  },
  {
    title: "Twitter",
    caption: "@quasarframework",
    icon: "rss_feed",
    link: "https://twitter.quasar.dev",
  },
  {
    title: "Facebook",
    caption: "@QuasarFramework",
    icon: "public",
    link: "https://facebook.quasar.dev",
  },
  {
    title: "Quasar Awesome",
    caption: "Community Quasar projects",
    icon: "favorite",
    link: "https://awesome.quasar.dev",
  },
];

import { defineComponent, ref } from "vue";
// import Footer from "app/my-app/src/components/Footer.vue";

export default defineComponent({
  name: "MainLayout",

  components: {
    EssentialLink,
    FooterLink,
    NavbarLink,
  },

  setup() {
    const leftDrawerOpen = ref(true);

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
