<template>
  <v-app>
     <v-app-bar
      app
      color="accent-4"
      light
      fixed
    >
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Mi app</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn plain>
        INICIO
      </v-btn>

      <v-btn plain>
        BUSCAR
      </v-btn>

      <v-btn plain>
        ACERCA DE
      </v-btn>
     
    </v-app-bar>

    <v-navigation-drawer
      app
      absolute
      dark
      src="https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg"
      width="20%"
      v-model="drawer" 
      temporary
    >
      <v-list>
        <v-list-item
          v-for="([icon, text], i) in items"
          :key="i"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ text }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <router-view/>
    </v-main>

    <v-footer
    color="primary lighten-1"
    padless
    class="mt-8"
  >
    <v-row
      justify="center"
      no-gutters
    >
      <v-col
        class="primary lighten-2 py-4 text-center white--text"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-col>
    </v-row>
  </v-footer>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    items: [
      ['mdi-email', 'Inbox'],
      ['mdi-account-supervisor-circle', 'Supervisors'],
      ['mdi-clock-start', 'Clock-in'],
    ],
    drawer: false,
    
    }),
};
</script>
