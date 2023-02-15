<template>
  <v-app-bar
    app
    color="white"
    light
    elevation="0"
    elevate-on-scroll
    style="padding: 0px 90px"
  >
    <v-toolbar-title class="font-weight-bold"> Devs </v-toolbar-title>
    <v-spacer></v-spacer>
    <v-list class="d-flex align-center">
      <v-list-item link v-for="(menu, i) in menus" :key="i" :to="menu.route">
        <v-list-item-title>{{ menu.title }}</v-list-item-title>
      </v-list-item>
      <v-btn>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
      <v-btn variant="outlined" color="success">Get Started</v-btn>
    </v-list>
  </v-app-bar>
</template>

<script>
export default {
  name: "HeaderComponent",
  data() {
    //
    return {
      menus: [
        { title: "Home", route: "home" },
        { title: "About us", route: "about us" },
        { title: "Portfolio", route: "portfolio" },
        { title: "Project", route: "project" },
        { title: "Gallery", route: "gallery" },
        { title: "Contact", route: "contact" },
      ],
    };
  },
};
</script>

<style></style>
