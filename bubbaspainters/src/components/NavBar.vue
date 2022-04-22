<template>
    <nav >
        <v-toolbar flat app>
            <v-app-bar-nav-icon @click="menu = !menu"></v-app-bar-nav-icon>
            <v-toolbar-title class="text-uppercase gray--text">
                <span>Bubba's</span>
                <span class="font-weight-light">Painting</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <span ><router-link to="/contact" class="text-decoration-none">Contact Us</router-link></span>
        <v-navigation-drawer app v-model="menu" >
        <v-list class="text-center">
        <v-img src='../images/logo.png'></v-img>
        <v-list-subheader class="text-h3 text-decoration-underline">Menu</v-list-subheader>
        <v-list-item
          v-for="(link, i) in links"
          :key="i"
          :value="item"
          active-color="primary"
          variant="plain"
          router :to="link.route"
        >
          <v-list-item-avatar start>
            <v-icon :icon="link.icon" flat app></v-icon>
          </v-list-item-avatar>
          <v-list-item-title v-text="link.text" @click="menu = !menu"></v-list-item-title>
        </v-list-item>
      </v-list>
        </v-navigation-drawer>
        </v-toolbar>
        
    </nav>
</template>
<script>


export default {
    data(){
        return{
            menu: false,
            links:[
                {icon: 'mdi-home', text: 'Home', route: '/'},
                {icon: 'mdi-account-tie', text: 'About Bubbas', route: '/about'},
                {icon: 'mdi-briefcase-outline', text: 'Our Work', route: '/work'},
                {icon: 'mdi-account-box', text: 'Contact Us', route: '/contact'},
            ]
        }
    }
}
</script>
