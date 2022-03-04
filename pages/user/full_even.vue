<template>
  <div>
    <v-toolbar
      color="indigo darken-4"
    >
      <v-toolbar-title>
        <v-btn href="/user/home" icon>
          <v-icon>mdi-chevron-left</v-icon>
        </v-btn>
      </v-toolbar-title>
&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp;
&nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;
      <v-spacer />
      <v-spacer />
    </v-toolbar><br><br>
    <div>
      <br><br>
      <v-card
        elevation="2"
        class="full"
      >
        <br><br>
        <h1 class="h1_1">จำนวนผู้เข้าร่วม</h1>
        <h2>500</h2>
        <br>
        <v-banner />
      </v-card><br>
      <h1 class="h1_2">สิทธิ์การเข้าร่วมเต็มแล้ว</h1>
    </div><br><br><br><br><br><br><br>
  </div>
</template>
<style>
.full{
   background: rgb(12, 11, 71);
    background: -webkit-linear-gradient(rgb(12, 11, 71),rgb(12, 11, 71));
    background: -o-linear-gradient(rgb(12, 11, 71), rgb(82, 80, 190));
    background: -moz-linear-gradient(rgb(12, 11, 71), rgb(82, 80, 190));
    background: linear-gradient(rgb(12, 11, 71), rgb(82, 80, 190));
}
.h1_2{
  color: rgb(95, 89, 89);
}
</style>
