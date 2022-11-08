<template>
<div>
    <v-navigation-drawer app v-model="drawer" temporary>
      <h3>This is one drawer for Options</h3>
    </v-navigation-drawer>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>
  <v-footer
    color="primary lighten-1"
    padless
  >
    <v-row
      justify="center"
      no-gutters
    >
      <v-btn
        v-for="link in links"
        :key="link"
        color="white"
        text
        rounded
        class="my-2"
      >
        {{ link }}
      </v-btn>
      <v-col
        class="primary lighten-2 py-4 text-center white--text"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-col>
    </v-row>
    
  </v-footer>
  <div>
    <v-toolbar
      dark
      prominent
      hide-on-scroll
      :collapse="drawer"
      src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
    >
      <v-app-bar-nav-icon @click="toggleDrawer()"></v-app-bar-nav-icon>

      <v-toolbar-items :allign="center">
       
            <v-btn
                v-for="link in links"
                :key="link"
                color="white"
                text
                rounded
                class="my-2"
            >
            {{ link }}
            </v-btn>     
      </v-toolbar-items>
      
      <v-spacer/>

      <v-btn icon>
        <v-icon>mdi-share</v-icon>
      </v-btn>
    </v-toolbar>
  </div>
</div>
</template>

<script>
  export default {
    data: () => ({
    drawer: false,
    links: [
        'Home',
        'About Us',
        'Blog',
        'Contact Us',
      ],
    }),
    methods: {
        toggleDrawer() {
            this.drawer = !this.drawer
        }
    }
  }
</script>
