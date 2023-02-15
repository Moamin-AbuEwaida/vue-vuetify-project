<template>
  <v-container class="my-15">
    <v-row justify="center">
      <v-col lg="12" class="text-center">
        <v-subheader class="text-h4">Portfolio</v-subheader>
        <p class="my-2">
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Adipisci,
          libero!
        </p>
      </v-col>
      <v-col lg="12">
        <div class="text-center">
          <v-chip
            @click="activePortfolio = 'webapp'"
            :color="activePortfolio === 'webapp' ? 'success' : ''"
            class="mx-5"
            >Web App</v-chip
          >
          <v-chip
            @click="activePortfolio = 'mobileapp'"
            :color="activePortfolio === 'mobileapp' ? 'success' : ''"
            class="mx-5"
            >Mobile App</v-chip
          >
          <v-chip
            @click="activePortfolio = 'desktopapp'"
            :color="activePortfolio === 'desktopapp' ? 'success' : ''"
            class="mx-5"
            >Desktop App</v-chip
          >
        </div>
      </v-col>
      <slot v-if="activePortfolio === 'webapp'">
        <v-col lg="3" v-for="(web, i) in webApps" :key="i">
          <v-card>
            <v-img
              :src="web.image"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="200px"
              cover
            >
              <v-card-title class="text-white">{{ web.title }}</v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </slot>
      <slot v-if="activePortfolio === 'mobileapp'">
        <v-col lg="3" v-for="(mob, i) in mobileApps" :key="i">
          <v-card>
            <v-img
              :src="mob.image"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="200px"
              cover
            >
              <v-card-title class="text-white">{{ mob.title }}</v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </slot>
      <slot v-if="activePortfolio === 'desktopapp'">
        <v-col lg="3" v-for="(desk, i) in deskApps" :key="i">
          <v-card>
            <v-img
              :src="desk.image"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="200px"
              cover
            >
              <v-card-title class="text-white">{{ desk.title }}</v-card-title>
            </v-img>
          </v-card>
        </v-col>
      </slot>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "PortfolioComponent",
  data() {
    return {
      activePortfolio: "webapp",
      webApps: [
        {
          title: "Web App1",
          image:
            "https://p.kindpng.com/picc/s/115-1151241_download-responsive-web-design-png-image-website-design.png",
        },
        {
          title: "Web App2",
          image:
            "https://p.kindpng.com/picc/s/115-1151601_vacation-labs-travel-website-and-booking-engine-website.png",
        },
        {
          title: "Web App3",
          image:
            "https://p.kindpng.com/picc/s/124-1247059_view-website-on-screens-desktop-hd-png-download.png",
        },
        {
          title: "Web App4",
          image:
            "https://p.kindpng.com/picc/s/124-1246957_premium-matching-gift-plugin-header-image-donate-to.png",
        },
        {
          title: "Web App5",
          image:
            "https://p.kindpng.com/picc/s/140-1404818_website-creation-hd-png-download.png",
        },
        {
          title: "Web App6",
          image:
            "https://p.kindpng.com/picc/s/490-4908087_ecommerce-website-hd-png-download.png",
        },
        {
          title: "Web App7",
          image:
            "https://p.kindpng.com/picc/s/193-1936903_responsive-design-website-ecommerce-website-design-hd-png.png",
        },
      ],
      mobileApps: [
        {
          title: "Mobile App 1",
          image:
            "https://p.kindpng.com/picc/s/9-94860_mobile-app-development-hd-png-download.png",
        },
        {
          title: "Mobile App 2",
          image:
            "https://p.kindpng.com/picc/s/15-155768_create-a-sports-app-hd-png-download.png",
        },
        {
          title: "Mobile App 3",
          image:
            "https://p.kindpng.com/picc/s/9-95536_app-development-mobile-app-image-png-transparent-png.png",
        },
        {
          title: "Mobile App 4",
          image:
            "https://p.kindpng.com/picc/s/9-95066_refill-app-refill-assistant-iphone-samsung-galaxy-hd.png",
        },
        {
          title: "Mobile App 5",
          image:
            "https://p.kindpng.com/picc/s/111-1117281_mobile-app-screens-png-transparent-png.png",
        },
        {
          title: "Mobile App 6",
          image:
            "https://p.kindpng.com/picc/s/9-95710_phone-in-hand-png-transparent-png.png",
        },
        {
          title: "Mobile App 7",
          image:
            "https://p.kindpng.com/picc/s/15-156505_mobile-apps-iphone-hd-png-download.png",
        },
      ],
      deskApps: [
        {
          title: "Desktop App 1",
          image:
            "https://p.kindpng.com/picc/s/197-1977529_time-timer-desktop-app-time-timer-windows-app.png",
        },
        {
          title: "Desktop App 2",
          image:
            "https://p.kindpng.com/picc/s/160-1605718_transparent-messages-icon-png-google-inbox-png-download.png",
        },
        {
          title: "Desktop App 3",
          image:
            "https://p.kindpng.com/picc/s/332-3327749_smart-widget-on-desktop-ios-and-android-led.png",
        },
        {
          title: "Desktop App 4",
          image:
            "https://p.kindpng.com/picc/s/634-6348668_view-and-export-prototypes-on-desktop-and-movile.png",
        },
        {
          title: "Desktop App 5",
          image:
            "https://p.kindpng.com/picc/s/20-204419_livechat-for-windows-live-chat-desktop-app-hd.png",
        },
        {
          title: "Desktop App 6",
          image:
            "https://p.kindpng.com/picc/s/577-5776997_vue-app-with-the-auth0-login-button-nw.png",
        },
        {
          title: "Desktop App 7",
          image:
            "https://p.kindpng.com/picc/s/493-4933583_best-mac-apps-and-utilities-beautiful-mac-os.png",
        },
      ],
    };
  },
};
</script>

<style></style>
