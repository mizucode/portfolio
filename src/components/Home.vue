<template>
  <v-container style="padding-right: 3em; padding-left: 3em">
    <v-row class="text-center">
      <v-col cols="12">
        <v-banner class="mx-auto" max-width="300" height="200">
          <v-img id="ink-brush" :src="require('../assets/logo1.svg')">
          </v-img>
        </v-banner>
      </v-col>
      <v-col cols="4">
        <v-hover v-slot="{ hover }">
          <v-card class="mx-auto" max-width="344" height="217">
            <v-img
              :aspect-ratio="16 / 12"
              :src="require('../assets/github.svg')"
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
                  style="height: 100%; background-color: #8eb894"
                >
                  <v-card-text align="center">
                    <div class="my-4 text-subtitle-1">
                      take a look at the code behind my projects on github
                    </div>
                    <v-btn
                      auto
                      color="#608866"
                      class="white--text"
                      fab
                      elevation="5"
                      href="https://github.com/mizucode"
                    >
                      check it out >
                    </v-btn>
                  </v-card-text>
                </div>
              </v-scroll-x-reverse-transition>
            </v-img>
          </v-card>
        </v-hover>
      </v-col>
      <v-col cols="4">
        <v-hover v-slot="{ hover }">
          <v-card class="mx-auto" max-width="344" height="217">
            <v-img
              :aspect-ratio="16 / 12"
              :src="require('../assets/dnn_panda1.png')"
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
                  style="height: 100%; background-color: #8eb894"
                >
                  <v-card-text align="center">
                    <div class="my-4 text-subtitle-1">
                      image-better-upper is an app to transform old images into
                      high-resolution png files using Open CV's ESPCN model
                    </div>
                    <v-btn
                      color="#608866"
                      class="white--text"
                      fab
                      small
                      href="https://image-better-upper.mizucode.com"
                    >
                      check it out >
                    </v-btn>
                  </v-card-text>
                </div>
              </v-scroll-x-reverse-transition>
            </v-img>
          </v-card>
        </v-hover>
      </v-col>

            <v-col cols="4">
                <v-hover v-slot="{ hover }">
          <v-card class="pa-2" max-width="144" height="100">
            <v-img
              :aspect-ratio="16 / 12"
              :src="require('../assets/email_icon.jpg')"
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
                  style="height: 100%; background-color: #8eb894"
                >
                  <v-card-text>
                    
                    <v-btn
                      auto
                      color="#608866"
                      class="white--text"
                      fab
                      elevation="5"
                      href="mailto:sophie.mizucode.com"
                    >
                      send me <br>
                      an email
                    </v-btn>
                  </v-card-text>
                </div>
              </v-scroll-x-reverse-transition>
            </v-img>
          </v-card>
        </v-hover>
           <v-spacer>

           </v-spacer>
           <div><p>   </p></div>
  
        <v-hover v-slot="{ hover }">
          <v-card class="pa-2" max-width="144" height="100">
            <v-img
              :aspect-ratio="16 / 12"
              :src="require('../assets/linked-28.png')"
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
                  style="height: 100%; background-color: #8eb894"
                >
                  <v-card-text>
                    
                    <v-btn
                      auto
                      color="#608866"
                      class="white--text"
                      fab
                      elevation="5"
                      href="https://www.linkedin.com/in/sophie-as/"
                    >
                      message me <br>
                      on linkedin
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
export default {
  data: () => ({
    hover: true,
  }),
};
</script>
