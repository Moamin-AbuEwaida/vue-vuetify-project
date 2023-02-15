<template>
  <v-container class="my-15">
    <v-row justify="center">
      <v-col lg="12" class="text-center">
        <v-subheader class="text-h4 justify-center">Projects</v-subheader>
        <p class="my-2">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Mollitia,
          deserunt?
        </p>
      </v-col>
      <v-col lg="4" v-for="project in 3" :key="project">
        <v-card class="mx-auto my-12" max-width="374">
          <v-img cover height="250" src="../assets/web1.svg"></v-img>

          <v-card-title>Web Development</v-card-title>

          <v-card-text>
            <div>
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Temporibus, repudiandae facere tempore fugit laborum perferendis.
            </div>
          </v-card-text>
          <v-divider class="mx-4 mb-1"></v-divider>
          <v-card-cations>
            <div class="d-flex p-2">
              <v-btn variant="text" color="success" rounded class="m-2"
                >View Details</v-btn
              >
              <v-spacer />
              <v-rating
                :model-value="4.5"
                color="amber"
                density="compact"
                half-increments
                readonly
                size="small"
              ></v-rating>
            </div>
          </v-card-cations>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "ProjectComponent",
};
</script>

<style></style>
