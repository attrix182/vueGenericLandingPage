<template>
  <v-container>
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

        <v-form ref="form" v-model="valid" lazy-validation>
          <v-text-field v-model="email" label="E-mail" required></v-text-field>

          <v-text-field
            v-model="password"
            :counter="10"
            label="Password"
            required
          ></v-text-field>

          <v-col class="mb-4">
            <v-btn color="primary" elevation="11">LOG IN</v-btn>
          </v-col>
          <v-col class="mb-4">
            <div class="text-center">
              <v-dialog v-model="dialog" width="500">
                <template v-slot:activator="{ on, attrs }">
                  <v-btn
                    block
                    color="primary"
                    elevation="11"
                    v-bind="attrs"
                    v-on="on"
                    >Create New Account</v-btn
                  >
                </template>

                <v-card>
                  <v-card-title class="headline grey lighten-2">
                   Sign Up
                  </v-card-title>

                  <v-card-text>
                    <v-form ref="form" v-model="valid" lazy-validation>
                      <v-text-field
                        v-model="name"
                        :counter="10"
                        :rules="nameRules"
                        label="Name"
                        required
                      ></v-text-field>

                      <v-text-field
                        v-model="email"
                        :rules="emailRules"
                        label="E-mail"
                        required
                      ></v-text-field>



                       <v-text-field
                        v-model="password"
                        :type="'password'"
                        :rules="passwordRules"
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
        </v-form>
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
  name: "HelloWorld",

  data: () => ({}),
};
</script>
