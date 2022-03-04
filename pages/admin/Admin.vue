<template>
  <div>
    <center>
      <v-toolbar
        color="indigo darken-4"
      >
        <v-toolbar-title>ADMIN</v-toolbar-title>
&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp;
&nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;&nbsp; &nbsp;
        <v-spacer />
        <v-spacer />
        <v-btn icon href="/">
          <v-icon>mdi-export</v-icon>
        </v-btn>

        <v-spacer />
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

            <h1>admin{{ id }}</h1>
          </v-col>
        </v-row>
        <br>
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
          {{ id }} <br>
          1ผู้ที่เข้าใช้ไอดีนี้คือคนที่ได้รับอนุญาติให้ดูแลกิจกกรม <br>
          2หน้าแรกสามารแก้ไขหรือเพิ่มกิจกรรมได้ <br>
          3บุคคลที่ได้รับไอดีนี้สามารถเช็คผู้ใช้เราร่วมได้
        </h4>
        <br><br><br><br><br>
      </div>
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
      // this.id = this.$route.query.user_id
      const res = await fetch('http://localhost:7002/list_p?user_id=' + this.id)
      const data = await res.json()
      console.log('row=', data)
      this.f_name = data.rows[0][0].f_name
      this.l_name = data.rows[0][0].l_name
      this.id = data.rows[0][0].id
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
