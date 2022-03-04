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
      <v-card
        color="blue darken-4"
      >
        <v-responsive
          :aspect-ratio="10/5"
          elevation="10"
        >
          <v-card-text>
            <br>
            <h2>ผู้ลงชื่อเข้าร่วม</h2><br><br>
            <span class="num">115</span>
          </v-card-text>
        </v-responsive>
      </v-card>
      <div class="in">
        <br>
        <v-row>
          <v-col
            cols="12"
            md="4"
          >
            <v-text-field
              v-model="name"
              label="ชื่อนักศึกษา"
              placeholder="name"
              filled
              rounded
              background-color="light-blue darken-3"
            />
            <v-text-field
              v-model="name"
              class="id"
              label="รหัสนักศึกษา"
              placeholder="ID"
              filled
              rounded
              background-color="light-blue darken-3"
            />
          </v-col>
        </v-row>
        <v-row>
          <v-col
            cols="5"
            md="4"
          >
            <v-autocomplete
              v-model="num"
              label="เลขที่"
              filled
              rounded
              background-color="light-blue darken-3"
            />
          </v-col>
          <v-col>
            <v-autocomplete
              v-model="room"
              label="ห้อง"
              filled
              rounded
              background-color="light-blue darken-3"
            />
          </v-col>
        </v-row>
        <v-row>
          <v-col>
            <v-text-field
              v-model="name"
              class="n_p"
              label="แผนกนักศึกษา"
              placeholder="ID"
              filled
              rounded
              background-color="light-blue darken-3"
            />
          </v-col>
        </v-row>
        <v-btn
          class="btn_01"
          rounded
          color="lime lighten-1"
          filled
        >
          ลงทะเบียน
        </v-btn>
      </div>
    </div>
  </div>
</template>
<style>
.num{
  font-size: 10vh;
}
.id{
  margin-top: 10vh;
}
ิ.btn_01{
  color: black;
  stroke: black ;
}
</style>
