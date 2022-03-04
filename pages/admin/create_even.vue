<template>
  <div>
    <div class="ha"><br>
      <v-btn
        icon
        color="indigo accent-2"
        dark
        absolute
        right
        fab
        left
        href="/admin/home_Admin"
      >
        <v-icon>mdi-chevron-left</v-icon>
      </v-btn>
    </div><br><br>
    <v-card
      class="mx-auto my-12"
      max-width="400"
      color="blue-grey lighten-2"
    >
      <br>
      <v-text-field
        v-model="user"
        label="ชื่อกิจกรรม"
        filled
        rounded
        dense
      />
      <v-text-field
        v-model="user"
        label="วัน/เวลา"
        filled
        rounded
        dense
      />
      <v-text-field
        v-model="user"
        label="สถานที่"
        filled
        rounded
        dense
      />
      <v-text-field
        v-model="user"
        label="จำนวนผู้เข้าร่วม"
        filled
        rounded
        dense
      /> <br><br>
      <div class="btn1">
        <v-btn
          rounded
          color="blue darken-4"
        >
          สร้าง
        </v-btn>
        <br>
      </div><br><br>
    </v-card>
  </div>
</template>
<style>
.icon{
   margin: 1vh;
   width:30vh;
 }
</style>
