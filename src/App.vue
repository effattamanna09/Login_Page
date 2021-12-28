<template>
  <v-app>
    <div class="background"></div>

    <v-main class="d-flex justify-center align-center">
      <v-col cols="10" lg="4" class="mx-auto">
        <v-card class="pa-4">
          <div class="text-center">
            <v-avater size="100" color="indigo lighten-4">
              <v-icon size="40" color="indigo">mdi-account</v-icon>
            </v-avater>
            <h2 class="indigo--text">Vue Login Page</h2>
          </div>
          <v-form>
            <v-card-text>
              <v-text-field
                type="email"
                lable="Email"
                placeholder="Email"
                prepend-inner-icon="mdi-account"
              />

              <v-text-field
                :type="passwordShow ? 'text' : 'password'"
                lable="Password"
                placeholder="Password"
                prepend-inner-icon="mdi-key"
                :append-icon="passwordShow ? 'mdi-eye' : 'mdi-eye-off'"
                @click:append="passwordShow = ! passwordShow"
              />
              <v-switch label="Remember me" color="indigo" >
              </v-switch>
            </v-card-text>
            <v-card-actions class="justify-center">
              <v-btn color="indigo">
                <span class="white--text px-8">Login</span>
              </v-btn>
            </v-card-actions>
          </v-form>
        </v-card>
      </v-col>
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",
  data: ()=> ({
   passwordShow: false,
  }),
};
</script>

<style scope>
.background {
  background-image: url(./assets/bg.jpg) !important;
  height: 300px;
  width: 100%;
  display: block;
  position: absolute;
  background-size: cover;
}
</style>
