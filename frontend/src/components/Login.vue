<template>
  <v-container>
    <div class="modalSignUp">
      <v-col class="mb-6">
        <div class="text-center">
          <v-dialog v-model="dialog" width="600">
            <template v-slot:activator="{ on, attrs }">
              <v-btn
                block
                color="primary"
                elevation="15"
                v-bind="attrs"
                v-on="on"
                >Create New Account</v-btn
              >
            </template>

            <v-card>
              <v-card-title class="headline blue darken-2 lighten-2">
                Sign Up
              </v-card-title>

              <v-card-text>
                <v-form ref="formRegister">
                  <v-text-field label="Name" required></v-text-field>

                  <v-text-field label="Lastname" required></v-text-field>

                  <v-text-field
        
                    label="E-mail"
                    required
                  ></v-text-field>

                  <v-text-field
          
                    :type="'password'"
                    label="Password"
                    required
                  ></v-text-field>
                </v-form>
              </v-card-text>

              <v-divider></v-divider>

              <v-card-actions>
                <v-spacer></v-spacer>

                <v-btn color="primary" text @click="dialog = false">
                  Continue
                </v-btn>
              </v-card-actions>
            </v-card>
          </v-dialog>
        </div>
      </v-col>
    </div>

    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/signUp2.png')"
          class="my-3"
          contain
          height="250"
        />
      </v-col>

      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">Welcome</h1>

        <div class="loginForm">
          <v-form ref="formLogin">
            <v-text-field label="E-mail" required>
            </v-text-field>

            <v-text-field
   
              label="Password"
              type="password"
              required
            ></v-text-field>

            <v-col class="mb-4">
              <v-btn block color="primary" elevation="15">LOG IN</v-btn>
            </v-col>
            <div class="btnsForgot">
              <v-row no-gutters>
                <v-col order="first">
                  <v-btn x-small color="primary" dark elevation="10">
                    Forgot Pass?
                  </v-btn>
                </v-col>
                <v-col order="last">
                  <v-btn x-small color="primary" dark elevation="10">
                    Forgot Email?
                  </v-btn>
                </v-col>
              </v-row>
            </div>
          </v-form>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>





<script>
export default {
  data() {
    return {
      dialog: false,
    };
  },
};
</script>


<script>
export default {
  name: "Login",

  data: () => ({}),
};
</script>
