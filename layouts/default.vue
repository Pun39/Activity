<template>
  <v-app>
    <v-container class="bg blue lighten-5 darken-2 text-center">
      <span class="white--text">
        <v-container>
          <Nuxt />
        </v-container>
      </span>
    </v-container>
  </v-app>
</template>
<style>
.bg{
   background: rgb(5, 14, 93);
    background: -webkit-linear-gradient(rgb(5, 14, 93), rgb(64, 54, 194));
    background: -o-linear-gradient(rgb(5, 14, 93), rgb(64, 54, 194));
    background: -moz-linear-gradient(rgb(5, 14, 93), rgb(255, 255, 255));
    background: linear-gradient(rgb(5, 14, 93), rgb(255, 255, 255));
}
</style>
