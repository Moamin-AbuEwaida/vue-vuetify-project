<template>
  <v-container class="pt-15">
    <v-row>
      <v-col lg="6" class="d-flex flex-column align-center justify-center">
        <h2 class="text-h2 font-weight-bold text-grey-darken-2">
          Welcome to the App
        </h2>
        <p class="my-4 text-grey-darken-4">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores
          praesentium vel aspernatur ut quia optio maxime enim doloremque odio
          doloribus.
        </p>
        <div>
          <v-btn class="white--color mr-10" color="success" rounded
            >Get Started</v-btn
          >
          <v-btn class="white--color" color="indigo" rounded>
            <v-icon>mdi-play-circle</v-icon> Watch Video
          </v-btn>
        </div>
      </v-col>
      <v-col lg="6">
        <v-img width="100%" src="./../assets/hero-banner.svg" alt="/"></v-img>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HeroComponent",
};
</script>

<style scoped></style>
