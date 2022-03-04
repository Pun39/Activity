<template>
  <div class="pa">
    <v-toolbar
      color="indigo darken-4"
    >
      <v-toolbar-title>ACTIVITY</v-toolbar-title>
&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp;
&nbsp;&nbsp; &nbsp;&nbsp;
      <v-spacer />
      <v-spacer />
      <v-btn v-model="sh" icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-spacer />
      <span class="subheading" />

      <v-spacer />
      <v-divider vertical />
      <v-app-bar-nav-icon />
    </v-toolbar><br><br>
    <div class="ij">
      <v-sheet
        color="indigo lighten-3"
        elevation="1"
        height="60"
        width="180"
        rounded="20"
      >
        <br>
        <h4 class="p1">
          กิจกรรมที่ลงชื่อแล้ว
        </h4>
        <br>
      </v-sheet><br>
      <v-sheet
        color="indigo lighten-4"
        elevation="1"
        height="150"
        width="300"
        rounded="20"
      >
        <br><br>
        <h1>กิจกรรม</h1> <br>
        <div class="p">
          <h4>ผ่าน&nbsp;&nbsp;&nbsp;&nbsp;</h4>
        </div>
        <br>
      </v-sheet><br>
      <v-sheet
        color="indigo lighten-3"
        elevation="1"
        height="60"
        width="180"
        rounded="20"
      >
        <br>
        <h4 class="p1">
          กิจกรรมที่รอเข้าร่วม
        </h4>
        <br>
      </v-sheet><br>
      <v-sheet
        color="indigo lighten-4"
        elevation="1"
        height="150"
        width="300"
        rounded="20"
      >
        <br><br>
        <h1>กิจกรรม</h1> <br>
        <div class="p">
          <h4>กำลังรอเข้าร่วม&nbsp;&nbsp;&nbsp;&nbsp;</h4>
        </div>
        <br>
      </v-sheet>
    </div><br>
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
        href="/user/user"
      >
        <v-icon>
          mdi-account
        </v-icon>
      </v-btn>
    </v-bottom-navigation>
  </div>
</template>
<style>
.p{
  text-align: right;
  color: #000;
}
h1{
  color: #000;
}
.p1{
  color: #000;
}
.pa{
  background-color: white;
}
</style>
