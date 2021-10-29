<template>
  <v-snackbar
    top
    right
    v-model="show"
  >
    {{ message }}

    <template v-slot:action="{ attrs }">
      <v-btn
        color="pink"
        text
        v-bind="attrs"
        @click="show = false"
      >
        Close
      </v-btn>
    </template>
  </v-snackbar>
</template>

<script>
export default {
  data () {
    return {
      show: false,
      message: '',
      color: ''
    }
  },
  created () {
    this.$store.subscribe((mutation, state) => {
      if (mutation.type === 'showMessage') {
        this.message = state.content
        this.color = state.color
        this.show = true
      }
    })
  }
}
</script>