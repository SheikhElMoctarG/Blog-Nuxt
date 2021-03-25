<template>
  <div class="all">
    <div class="header">
      <v-app-bar
      color="deep-purple accent-4"
      dense
      dark
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

      <v-toolbar-title>مدونة</v-toolbar-title>

      <v-spacer></v-spacer>

    </v-app-bar>
    </div>

    <Nuxt />
    <div class="footer">
      <v-footer class="con" padless>
    <v-col
      class="text-center"
      cols="12"
    >
      {{ new Date().getFullYear() }} — <strong>My Blog</strong>
    </v-col>
  </v-footer>
    </div>
  </div>
</template>


<style>
@import url('https://fonts.googleapis.com/css2?family=Tajawal&display=swap');
.all{
  width: 500px;

}
.header{
  width: 500px;
  display: flex;
  align-items: center;
  justify-items: center;
}
.con{
  width: 500px;
  text-align: center;
}
html {
  font-family: 'Tajawal', sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  display: flex;
  align-items: center;
  justify-content: center;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
