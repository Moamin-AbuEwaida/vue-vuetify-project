<template>
  <v-container class="my-15">
    <v-row>
      <v-col lg="12" class="text-center">
        <v-subheader class="text-h4 justify-center">Contact Us</v-subheader>
        <p class="my-2">
          Lorem, ipsum dolor sit amet cong elit. Sapiente, dolore.
        </p>
      </v-col>
      <v-col lg="6">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d80598.4484100242!2d4.30537712201104!3d50.85521141089653!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47c3a4ed73c76867%3A0xc18b3a66787302a7!2sBrussels!5e0!3m2!1sen!2sbe!4v1676466675084!5m2!1sen!2sbe"
          width="100%"
          height="100%"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
      </v-col>
      <v-col lg="6">
        <v-form ref="form">
          <v-text-field
            v-model="contactInfo.name"
            label="Name"
            required
          ></v-text-field>
          <v-text-field
            v-model="contactInfo.email"
            label="Email"
            required
          ></v-text-field>
          <v-textarea
            label="Message"
            v-model="contactInfo.message"
          ></v-textarea>

          <div class="d-flex flex-column">
            <v-btn color="success" class="mt-4"> Send </v-btn>
          </div>
        </v-form>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "ContactUsComponent",
  data() {
    return {
      contactInfo: {},
    };
  },
};
</script>

<style></style>
