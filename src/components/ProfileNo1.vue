<template>
  <v-app>
    <v-navigation-drawer app v-model="drawer" clipped>Navigation Lists</v-navigation-drawer>
    <v-app-bar color="primary" dark app clipped-left>
      <v-app-bar-nav-icon @click="drawer=!drawer"></v-app-bar-nav-icon>
      <v-toolbar-title>My Page</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items>
      <v-btn color="primary" v-for="item in items" :key="item">{{ item.name }}</v-btn>
      </v-toolbar-items>
    </v-app-bar>
    <v-footer color="primary" dark app>
      Vuetify
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data(){
    return{
      drawer: false,
      items: [
        {name: 'Profile',},
        {name: 'Works'},
        {name: 'Skil'},
        {name: 'Contact'}
      ]
    }
  }
}
</script>