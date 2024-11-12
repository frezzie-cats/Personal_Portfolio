<template>
    <v-footer color="black" padless>
      <v-col
        class="text-center"
        cols="12"
        style="background-color: black; padding: 16px;"
      >
        <v-row justify="center" align="center" class="my-2">
          <v-icon color="#8e44ad" class="mx-2">mdi-github</v-icon>
          <v-icon color="#8e44ad" class="mx-2">mdi-linkedin</v-icon>
          <v-icon color="#8e44ad" class="mx-2">mdi-twitter</v-icon>
        </v-row>
        <p style="color: white; font-size: 0.9rem;">
          © {{ new Date().getFullYear() }} Frezzie Catamora. All Rights Reserved.
        </p>
      </v-col>
    </v-footer>
  </template>
  
  <script>
  export default {
    name: "Footer",
  };
  </script>
  
  <style scoped>
  .v-footer {
    color: white;
  }
  </style>
  