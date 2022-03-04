<template>
  <div>
    <v-toolbar
      color="indigo darken-4"
    >
      <br>
      <v-toolbar-title>
        CALENDAR
      </v-toolbar-title>
&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp;
&nbsp;&nbsp; &nbsp;&nbsp;
      <v-spacer />
      <v-icon>mdi-magnify</v-icon>

      <v-spacer />
      <span class="subheading" />

      <v-spacer />
      <v-divider vertical />
      <v-app-bar-nav-icon />
    </v-toolbar><br><br>
    <div class="rg ">
      <v-row justify="center ">
        <v-date-picker v-model="picker" />
      </v-row><br><br><br><br><br>
      <v-bottom-navigation
        absolute
        hide-on-scroll
        horizontal
        scroll-target="#hide-on-scroll-example"
      >
        <v-btn
          color="cyan lighten-5"
          text
          href="/user/home"
        >
          <v-icon>
            mdi-home
          </v-icon>
        </v-btn>

        <v-btn
          color="cyan lighten-5"
          text
          href="/user/cal"
        >
          <v-icon>mdi-calendar-month</v-icon>
        </v-btn>
        <v-btn
          color="cyan lighten-5"
          text
          href="/user/us_in"
        >
          <v-icon>
            mdi-account
          </v-icon>
        </v-btn>
      </v-bottom-navigation>
    </div>
  </div>
</template>
<script>
export default {
  data () {
    return {
      picker: (new Date(Date.now() - (new Date()).getTimezoneOffset() * 60000)).toISOString().substr(0, 10)
    }
  }
}
</script>
<style>
.rg{
  color: black;
  background-color: beige;
}
</style>
