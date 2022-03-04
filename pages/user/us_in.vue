<template>
  <div>
    <center>
      <v-toolbar
        color="indigo darken-4"
      >
        <v-toolbar-title>USER</v-toolbar-title>
&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp;
&nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;
        <v-spacer />
        <v-spacer />
        <v-btn icon href="/">
          <v-icon>mdi-export</v-icon>
        </v-btn>
      </v-toolbar><br><br>

      <div class="h">
        <v-row>
          <v-col>
            <img
              src="@/assets/img/02.jpg"
              width="50%"
            >
          </v-col>
          <v-col>
            <form action="">
              <v-icon>
                mdi-circle-edit-outline
              </v-icon>
            </form>
            <div>
              <h1>{{ f_name }}</h1>
            </div>
          </v-col>
        </v-row>
        <v-sheet
          color="blue-grey lighten-3"
          elevation="1"
          height="100"
          outlined
          rounded
          width="300"
        >
          <v-row>
            <v-col cols="6" md="8" />
            <v-col class="j3" cols="3" md="2" black>
              1
            </v-col>
            <v-col class="j3" cols="1" md="2" black>
              2
            </v-col>
          </v-row>
          <v-row>
            <v-col class="j3" cols="6" md="8">
              กิจกรรมที่เข้าร่วมแล้ว
            </v-col>
            <v-col class="l1" cols="3" md="2">
              <h3>/</h3>
            </v-col>
            <v-col class="l1" cols="1" md="2">
              <h3>/</h3>
            </v-col>
          </v-row>
        </v-sheet><br>
        <v-sheet
          color="indigo darken-4"
          elevation="1"
          height="50"
          outlined
          rounded
          width="300"
        >
          <h2>ข้อมูลส่วนตัว</h2>
        </v-sheet>
        <h4>
          ชื่อ {{ f_name }} {{ l_name }} <br>
          ที่อยู่ ..... <br>
          อำเภอ.....<br>
          จังหวัด .....<br>
        </h4>
        <br><br><br><br><br>
      </div>
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
          <v-icon>mdi-calendar-check-outline</v-icon>
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
    </center>
  </div>
</template>
<script>
export default {
  data: () => ({
    id: '',
    l_name: '',
    f_name: ''

  }),
  created () {
    this.Sh()
  },
  methods: {
    async Sh () {
      console.log('show')
      this.id = this.$route.query.user_id
      const res = await fetch('http://localhost:7002/list_t?user_id=' + this.id)
      const data = await res.json()
      console.log('row=', data)
      this.f_name = data.rows[0][0].f_name
      this.l_name = data.rows[0][0].l_name
    }
  }

}
</script>
<style>
.h{
  background-color: white;
}
 .pa-1{
  background:image(".../assets/02.jpg");
  width: 10vh;
  height: 10vh;
 }
 .icon{
   margin: 2vh;
   width: 25vh;
 }
 h1{
   color: black;
 }
 .l1{
   color: green;
 }
 .j3{
   color: black;
 }
 h2{
   color: white;
   text-align: left;
   margin: 1vh;
 }
 h4{
   color: black;
   text-align: left;
   margin: 4vh;
 }
</style>
