<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <h1 class="display-2 font-weight-bold mb-3" style="padding-top: 1em">
          Welcome to Vuetify
        </h1>

        <p class="subheading font-weight-regular">
          For help and collaboration with other Vuetify developers,
          <br />please join our online
          <a href="https://community.vuetifyjs.com" target="_blank"
            >Discord Community</a
          >
        </p>
      </v-col>
      <v-col v-for="n in 5" :key="n" cols="4">
        <v-hover v-slot="{ hover }">
          <v-card class="mx-auto" max-width="344" height="200">
            <v-img
              :aspect-ratio="16 / 12"
              src="https://cdn.vuetifyjs.com/images/cards/kitchen.png"
            >
              <v-scroll-x-reverse-transition>
                <div
                  v-if="hover"
                  class="
                    d-flex
                    transition-fast-in-fast-out
                    orange
                    darken-2
                    v-card--reveal
                    text-h2
                    white--text
                  "
                  style="height: 100%"
                >
                  $14.99
                  <v-btn
                    auto
                    color="orange"
                    class="white--text"
                    fab
                    elevation="5"
                    href="http://image-better-upper.mizucode.com"
                  >
                    check it out >
                  </v-btn>
                </div>
              </v-scroll-x-reverse-transition>
            </v-img>
          </v-card>
        </v-hover>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    hover: true,
  }),
};
</script>
