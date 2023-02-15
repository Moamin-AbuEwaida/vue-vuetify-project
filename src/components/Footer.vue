<template>
  <v-footer class="text-center d-flex flex-column">
    <v-col lg="12">
      <v-row justify="center">
        <v-col lg="4">
          <v-toolbar-title>Devs</v-toolbar-title>
          <!-- <v-card> -->
          <v-card-text>
            <v-btn
              v-for="icon in icons"
              :key="icon"
              class="mx-4"
              :icon="icon"
              variant="icon"
            ></v-btn>
          </v-card-text>
          <!-- </v-card> -->
          <v-subheader>Lorem ipsum, dolor sit amet consectetur a.</v-subheader>
        </v-col>
      </v-row>
    </v-col>
    <div></div>

    <v-divider></v-divider>

    <div>{{ new Date().getFullYear() }} — <strong>Devs</strong></div>
  </v-footer>
</template>

<script>
export default {
  name: "FooterComponent",
  data: () => ({
    icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"],
  }),
};
</script>

<style></style>
