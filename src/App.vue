<template>
  <v-app>
     <v-app-bar
      app
      color="accent-4"
      light
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>

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

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
};
</script>
