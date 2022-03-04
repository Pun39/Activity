<template>
  <div>
    <div class="text-center">
      <v-dialog
        v-model="dialog"
        width="500"
      >
        <v-card>
          <v-card-title class="text-h5 grey lighten-2">
            Status Login
          </v-card-title>

          <v-card-text>
            SUCCESS  LOGIN
          </v-card-text>

          <v-divider />

          <v-card-actions>
            <v-spacer />
            <v-btn
              color="primary"
              text
              @click="dialog = false"
            >
              I accept
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </div>
    <div class="text-center">
      <v-dialog
        v-model="dialog_false"
        width="500"
      >
        <v-card>
          <v-card-title class="text-h5 grey lighten-2">
            Status Login
          </v-card-title>

          <v-card-text>
            ERROR  LOGIN
          </v-card-text>

          <v-divider />

          <v-card-actions>
            <v-spacer />
            <v-btn
              color="primary"
              text
              @click="dialog_false = false"
            >
              I accept
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </div>
    <br>
    <center>
      <div
        class="pa-7 indigo darken-3 rounded-circle d-inline-block  filled "
      />
      <v-sheet
        color="white"
        height="50"
        rounded
        width="300"
      >
        <h1 class="h">
          กิจกรรมพิเศษ
        </h1>
      </v-sheet>
      <v-form>
        <div class="input">
          <br>
          <v-text-field
            v-model="std_id"
            label="เลขรหัสนักศึกษา"
            placeholder="ID"
            filled
            rounded
            dense
          />
          <br>
          <v-text-field
            v-model="pass"
            label="รหัสผ่าน/เลขประจำตัวประชาชน"
            placeholder="รหัสผ่าน"
            filled
            rounded
            dense
          />
          <br>
          <v-btn class="btn1" color="amber darken-2" @click="onSave">
            <span class="txt1">LOG IN</span>
          </v-btn> &nbsp; &nbsp;
        </div><br>
        <a>Forgot password?</a>
      </v-form>
      <br><br><br><br>
    </center>
  </div>
</template>
<script>
export default {
  data: () => ({
    id: ' ',
    std_id: '',
    pass: '',
    dialog: false,
    dialog_false: false
  }),
  methods: {
    async onSave () {
      console.log('onSave')
      const res = await fetch('http://localhost:7002/list?std_id=' +
              this.std_id + '&pass=' + this.pass)
      const result = await res.json()
      try {
        console.log('data=', result.data.u_status)
        if (result.status > 0) {
          console.log('Login ok')
          this.id = result.data.user_id
          this.dialog = true
          if (result.data.u_status === 'user') {
            this.$router.push('/user/us_in?user_id=' + this.id)
          } else if (result.data.u_status === 'admin') {
            this.$router.push('/admin/Admin')
          }
        }
      } catch (error) {
        console.log('Error Login' + error)
        this.dialog_false = true
        setInterval(() => {
          this.dialog_false = false
          this.$router.push('/')
        }, 3000)
      }
    }
  }

}
</script>
<style>
.pa-7{
  background: url('../assets/img/01.png');
  height: 33.5vh;
width:34vh;
}
.pa-2{
  border-radius: 10vh;
}
.txt1{
  color: rgb(255, 255, 255);
}
.btn1{
   background-color: rgb(223, 162, 19);
}
.h{
  color: rgb(19, 87, 104);
}
</style>
