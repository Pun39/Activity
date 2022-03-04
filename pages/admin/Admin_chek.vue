<template>
  <div>
    <v-toolbar
      color="indigo darken-4"
    >
      <v-toolbar-title>เช็คชื่อผู้เข้าร่วมกิจกรรม</v-toolbar-title>
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
    </v-toolbar>
    <div class="he">
      <v-card
        :loading="loading"
        class="mx-auto my-12"
        max-width="374"
        color="indigo lighten-5"
      >
        <div class="name">
          <v-row>
            <v-row align="center">
              <v-col
                class="d-flex"
                cols="5"
                sm="6"
              >
                <div class="j1">
                  <v-select
                    :items="items1"
                    label="ชื่อแผนก"
                    light
                    filled
                    rounded
                    dense
                  />
                </div>
              </v-col>

              <v-col
                class="d-flex"
                cols="3"
                sm="6"
              >
                <div class="j1">
                  <v-select
                    :items="items2"
                    label="ห้อง"
                    light
                    filled
                    rounded
                    dense
                  />
                </div>
              </v-col>

              <v-col
                class="d-flex"
                cols="3"
                sm="6"
              >
                <div class="j1">
                  <v-select
                    :items="items3"
                    label="เลขที่"
                    filled
                    rounded
                    dense
                    light
                  />
                </div>
              </v-col>
            </v-row>
          </v-row>
          <br><br><br><br><br><br><br><br><br><br><br><br><br><br>
          <br><br><br><br>
        </div>
      </v-card>
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
        href="/admin/home_admin"
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
<script>
export default {
  data: () => ({
    items1: ['บัญชี', 'ช่างยนต์', 'การตลาด ', 'IT', 'ไฟฟ้า'],
    items2: ['A1', 'A2', 'A3 ', 'B1', 'B2'],
    items3: ['1', '2', '3', '4', '5', '6', '7', '8', '9', '10']
  })
}
</script>
<style>

.icon{
   margin: 1vh;
   width:30vh;
 }
</style>
