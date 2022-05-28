<template>
  <div>
    <div>Zaloguj się emailem:
      <input type="email" v-model="email">
      <button @click="logIn()">{{buttonLabel}}</button>
    </div>
  </div>
</template>

<script>
import "milligram"

export default {
  data() {
    return {
      email: ''
    }
  },
  props: ['buttonLabel'],
  methods: {
    logIn() {
      this.$emit('login', this.email);
    }
  }
}
</script>


<style>

</style>
