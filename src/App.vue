<template>
  <v-app style="background-color: #000013">
    <v-main>
      <Home />
 
    </v-main>
      <v-footer
        color="#000013"
      >

        <v-dialog
          v-model="dialog"
          persistent
          max-width="600px"
        >
          <template v-slot:activator="{ on, attrs }">
          

            <v-btn
              v-for="icon in icons"
              :key="icon"
              class="mx-15 blue--text"
              icon
              v-bind="attrs"
              v-on="on"
              x-large
              
      
            >
              <v-icon left>
                {{ icon }}
              </v-icon>
              contact me
            </v-btn>
          </template>
          <v-card>
            <v-btn
              icon
              dark
              @click="dialog = false"
            >
              <v-icon>mdi-close</v-icon>
            </v-btn>
            <v-card-text>

                <div class="container">
                    <form @submit.prevent="sendEmail">
                                    <v-container>

                      <v-row>
                      <v-col
                        cols="12"
                        sm="8"
                        md="6"
                      >
                      <label>Name</label>
                      <input
                        type="text" 
                        v-model="name"
                        name="name"
                        outlined
                        placeholder="Your Name"
                        class="form-text"
                      >
                      </v-col>


                      <v-col cols="12" sm="8"
                        md="6">
                      <label>Email</label>
                      <input 
                        type="email" 
                        v-model="email"
                        name="email"
                        outlined
                        placeholder="Your Email"
                        class="form-text"
                        >
                      </v-col>
                      <v-col cols="9"
                      >
                          <label>Message</label>
                          <textarea
                            label="Message*" 
                            name="message"
                            v-model="message"
                            outlined
                            type="text"
                            placeholder="What would you like to discuss?"
                            >
                          </textarea>
                    </v-col>
                  </v-row>
                </v-container>

              <v-card-actions>

                      <v-card-text > <v-icon left

                          color="blue darken-1"
                        >
                          mdi-email
                        </v-icon> sophie@sophiecodes.com </v-card-text>
                      <input type="submit" @click="dialog = false" color="blue darken-1" value="Send Message">
                            </v-card-actions>

                    </form>
                </div>
                   
            </v-card-text>
          </v-card>
        </v-dialog>
          
      </v-footer>
  </v-app>
  
</template>

<script>
import Home from "./components/Home";
import emailjs from 'emailjs-com';

export default {
  name: "App",

  components: {
    Home,
  },

  data: () => ({
    dialog: false,
    icons: [
      'mdi-email-outline',
    ],
 
      name: '',
      email: '',
      message: ''
    
  }),

  methods: {
    sendEmail(e) {
      try {
        emailjs.sendForm('service_ffphltz', 'template_d4j2ays', e.target, 'user_8ZyEmnIIDNIsxUTE8hIE0', {
          name: this.name,
          email: this.email,
          message: this.meessage
        })

      } catch (error) {
          console.log({error})
      }
      // Reset form field
      this.name = ''
      this.email = ''
      this.message = ''
    },
  }
}
</script>
<style scoped>
* {box-sizing: border-box;}

label {
  float: left;
}
input[type=text], [type=email], textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid rgb(23, 154, 255);
  border-radius: 4px;

  background-color: aliceblue;
}

input[type=submit] {
  background-color: #2caeff;
  color: rgb(19, 0, 87);
  padding: 12px 20px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type=submit]:hover {
  background-color: #258eff;
}

.v-card {
  display: block;
  margin:auto;
  border-radius: 5px;
  background-color: #000013;

}
</style>
