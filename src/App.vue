<template>
  <v-app>
    <Snackbar/>
    
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <h1>vue-snack</h1>
      </div>
    </v-app-bar>

    <v-main>
      <router-view/>
    </v-main>
  </v-app>
</template>

<script>
import Snackbar from '@/components/Snackbar'
export default {
  name: 'App',

  components: {
    Snackbar,
  },

  data: () => ({
    //
  }),
};
</script>
