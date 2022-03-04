<template>
  <div>
    <v-toolbar
      color="indigo darken-4"
    >
      <v-toolbar-title>HOME</v-toolbar-title>
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
      <v-btn href="/" icon>
        <v-icon>mdi-export</v-icon>
      </v-btn>
    </v-toolbar>
    <center>
      <div class="ht2 indigo lighten-3">
        <br><br>
        <v-card-text style="height: 100px; position: relative">
          <v-fab-transition>
            <v-btn
              v-show="!hidden"
              color="indigo accent-2"
              dark
              absolute
              top
              right
              fab
              href="/admin/create_even"
            >
              <v-icon>mdi-plus</v-icon>
            </v-btn>
          </v-fab-transition>
        </v-card-text>
        <v-sheet
          color="indigo lighten-4"
          elevation="1"
          height="250"
          width="250"
          rounded="20"
        >
          <br><br>
          <h3 class="t1">
            &nbsp;&nbsp;กิจกรรม
          </h3> <br>
          <div class="p">
            <h3 class="p">
              &nbsp;&nbsp;ลอยกระทง
            </h3>
            <h4 class="p">
              &nbsp;&nbsp;รายละเอียด...
            </h4>
            <h4 class="p">
              &nbsp;&nbsp;จำนวน....
            </h4>
            <h4 class="p">
              &nbsp;&nbsp;เวลา....
            </h4>
          </div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          &nbsp;&nbsp;&nbsp;&nbsp;
          <v-btn class="btn blue darken-4" href="/admin/create_even" right>
            แก้ไข
          </v-btn>
          <br>
        </v-sheet><br>
        <v-sheet
          color="indigo lighten-4"
          elevation="1"
          height="250"
          width="250"
          rounded="20"
        >
          <br><br>
          <h3 class="t1">
            &nbsp;&nbsp;กิจกรรม
          </h3> <br>
          <div class="p">
            <h3 class="p">
              &nbsp;&nbsp;สถาปนา
            </h3>
            <h4 class="p">
              &nbsp;&nbsp;รายละเอียด...
            </h4>
            <h4 class="p">
              &nbsp;&nbsp;จำนวน....
            </h4>
            <h4 class="p">
              &nbsp;&nbsp;เวลา....
            </h4>
          </div>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          &nbsp;&nbsp;&nbsp;&nbsp;
          <v-btn
            class="btn blue darken-4"
            href="/admin/create_even"
            right
          >
            แก้ไข
          </v-btn>
          <br>
        </v-sheet>
      </div>
    </center>
    <v-bottom-navigation
      absolute
      hide-on-scroll
      horizontal
      scroll-target="#hide-on-scroll-example"
      color="blue darken-2"
    >
      <v-btn
        color="deep-purple accent-4"
        text
        href="/admin/home_admin"
        rounded
      >
        <v-icon>
          mdi-home
        </v-icon>
      </v-btn>

      <v-btn
        color="deep-purple accent-4"
        text
        href="/admin/Admin_chek"
        rounded
      >
        <v-icon>mdi-calendar-check-outline</v-icon>
      </v-btn>
      <v-btn
        color="deep-purple accent-4"
        text
        href="/admin/Admin"
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

.icon{
   margin: 1vh;
   width:30vh;
 }
.t1{
  text-align: left;
  color: black;
}
.btn1{
  text-align: right;
}
.h4{
  color: aliceblue;
}
.p{
  color: rgba(0, 0, 0, 0.541);
  text-align: left;
}
.btn{
  text-align: right;
}
</style>
