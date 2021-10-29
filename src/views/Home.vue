<template>
  <div>
    <v-btn color="primary" @click="showSnackbar">
      Show snackbar
    </v-btn>
  </div>
</template>

<script>

  export default {
    name: 'Home',

    methods: {
      showSnackbar () {
        this.$snackbar.showMessage({
          content: 'Hello, snackbar',
          color: 'info'
        })
      }
    }
  }
</script>
