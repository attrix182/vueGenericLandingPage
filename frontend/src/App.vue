<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <v-avatar color="gray">
        <v-icon dark> mdi-account-circle </v-icon>
      </v-avatar>

      <v-spacer></v-spacer>
    </v-app-bar>

    <v-main>
      <Login />
    </v-main>
  </v-app>
</template>

<script>
import Login from "./components/Login";

export default {
  name: "App",

  components: {
    Login,
  },

  data: () => ({
    //
  }),
};
</script>
