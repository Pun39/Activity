<template>
  <div>
    <center>
      <v-toolbar
        color="indigo darken-4"
      >
        <v-toolbar-title>HOME</v-toolbar-title>
&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp;
&nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;
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

      <div>
        <v-sheet
          color="white"
          elevation="10"
          height="400"
          rounded
          width="250"
        >
          &nbsp;&nbsp;
          <h2 class="t2">
            &nbsp;&nbsp;  กิจกรรม
          </h2> &nbsp;&nbsp;
          <h3 class="t2">
            &nbsp;&nbsp;  ลอยกระทง<br>
          </h3>
          <div class="u">
            <h4>&nbsp;&nbsp;รายละเอียด...........</h4>  <br>
            <h4> &nbsp;&nbsp;วันเวลา.......</h4> <br>
            <h4>  &nbsp;&nbsp; จำนวน</h4>
          </div><br><br><b /> &nbsp;&nbsp;  &nbsp;&nbsp;  &nbsp;&nbsp;  &nbsp;&nbsp;
          &nbsp;&nbsp;  &nbsp;&nbsp;  &nbsp;&nbsp;  &nbsp;&nbsp;
          <v-btn href="register_even" class="btn01 blue darken-1 rounded" right>
            เข้าร่วม
          </v-btn>
        </v-sheet>
        <br><br>
      </div>
    </center>

    <v-bottom-navigation
      absolute
      hide-on-scroll
      horizontal
      scroll-target="#hide-on-scroll-example"
    >
      <v-btn
        color="deep-purple accent-4"
        text
        href="/user/home"
        rounded
      >
        <v-icon>
          mdi-home
        </v-icon>
      </v-btn>

      <v-btn
        color="deep-purple accent-4"
        text
        href="/user/cal"
        rounded
      >
        <v-icon>mdi-calendar-check-outline</v-icon>
      </v-btn>
      <v-btn
        color="deep-purple accent-4"
        text
        href="/user/us_in"
        rounded
      >
        <v-icon>
          mdi-account
        </v-icon>
      </v-btn>
    </v-bottom-navigation>
  </div>
</template>
<style>
 h3{
   color: rgba(36, 32, 32, 0.712);
 }
 v-icon{
   color: black;
 }
 v-sheet{
   border-radius: 5vh ;
 }
 .t{
   border:5vh ;
 }

 .icon{
   margin: 2vh;
   width: 30vh;
 }
v-tabs{
  margin-left: 50vh;
}
.u{
  color: rgb(121, 116, 116);
  text-align: left;
}
.t2{
  color: black;
  text-align: left;
}
.btn01{
  text-align: right;
}
</style>
