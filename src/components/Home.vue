<template>
  <v-container style="padding-right: 3em; padding-left: 3em; background-color: #000013">
    <v-row class="text-center">
      <v-col cols="12">
        <v-banner class="mx-auto" max-width="300" height="200" style ="padding:35px !important">
          <vue-typer 
              :src="require('../assets/style.css')"
              :text='["<sophiecodes>"]'
              
              :pre-type-delay='70'
              :type-delay='70'
              :pre-erase-delay ='90000'
              caret-animation='blink'></vue-typer>
        </v-banner>
      </v-col>
      <v-col cols="6">
        <v-hover v-slot="{ hover }">
          <v-card class="mx-auto" max-width="344" height="217">
            <v-img
              :aspect-ratio="16 / 12"
              :src="require('../assets/butterfly.png')"
              height="100%"
            >
              <v-scroll-x-reverse-transition>
                <div
                  v-if="hover"
                  class="
                    d-flex
                    transition-fast-in-fast-out
                    v-card--reveal
                    white--text
                  "
                  style="height: 100%"
                >
                  <v-card-text align="center">
                    <div class="my-4 text-subtitle-1">
                      Image-better-upper transforms <br>small images into
                      high-resolution <br> png files using Open CV's ESPCN 
                    </div>
                    <v-btn 
                      color="#BD13FF"
                      class="white--text"
                      small
                      href="https://imagebetter.sophicodes.com"
                    >
                    <v-icon color="#000013">mdi-arrow-right</v-icon>
                  
                    </v-btn>
                  </v-card-text>
                </div>
              </v-scroll-x-reverse-transition>
            </v-img>
          </v-card>
        </v-hover>
      </v-col>
      <v-col cols="6">
        <v-hover v-slot="{ hover }">
          <v-card class="mx-auto" max-width="344" height="217">
            <v-img
              :aspect-ratio="16 / 12"
              :src="require('../assets/github.png')"
              height="100%"
            >
              <v-scroll-x-reverse-transition>
                <div
                  v-if="hover"
                  class="
                    d-flex
                    transition-fast-in-fast-out
                    v-card--reveal
                    white--text
                  "
                  style="height: 100%"
                >
                  <v-card-text align="center">
                    <div class="my-4 text-subtitle-1">
                      <br>The code behind it all <br>(my github)
                    </div>
                    <v-btn 
                      color="#BD13FF"
                      class="white--text"
                      small
                      href="https://github.com/sophie-arsenault"
                    >
                    <v-icon color="#000013">mdi-arrow-right</v-icon>
                  
                    </v-btn>
                  </v-card-text>
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

import Vue from 'vue'
import Vuetify from 'vuetify/lib'
import VueTyper from 'vue-typer'

Vue.use(Vuetify)
Vue.use(VueTyper)

export default new Vuetify({
  theme: { dark: true },
  data: () => ({
    hover: true,
    
  }),
})

</script>
