<template>
  <v-app>
      <v-app-bar app color="green" dark>
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
      <v-toolbar-title>
        Campeonato Brasileiro ⚽
      </v-toolbar-title>
    </v-app-bar>
    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary
    >
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="green--text text--lighten-2"
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Início</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-soccer</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Classificação</v-list-item-title>
          </v-list-item>

        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <Inicio/>
    </v-main>
  </v-app>
</template>

<script>
import Inicio from './components/Inicio'

export default {
  name: 'App',
  components: {
    Inicio
  },
  data: () => ({
    drawer: false,
    group: null,
  }),
};
</script>
