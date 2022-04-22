<template>
  <v-app>
    <nav-bar/>

    <v-content> <router-view/> </v-content>
  </v-app>
</template>

<script>
// import HomeView from './views/HomeView.vue'
// import MyWork from './views/MyWork.vue'
// import ContactView from './views/ContactView.vue' 
import NavBar from './components/NavBar.vue'

export default {
  name: 'App',

  data: () => ({
    //
  }),
  components:{
    NavBar,
  }
}
</script>
