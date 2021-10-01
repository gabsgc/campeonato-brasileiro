<template>
  <v-app>
      <AppTopBar/>
      <Inicio/>
  </v-app>
</template>

<script>
import Inicio from './components/Inicio'
import AppTopBar from './components/shared/AppTopBar'

export default {
  name: 'App',
  components: {
    Inicio,
    AppTopBar
  }
};
</script>
