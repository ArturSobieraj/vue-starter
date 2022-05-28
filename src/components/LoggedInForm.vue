<template>
  <div>
    <h2>Witaj {{email}}</h2>
    <a @click="logOut()">Wyloguj</a>
  </div>
</template>

<script>
import "milligram";

export default {
  name: "LoggedInForm",
  props: ['email'],
  methods: {
    logOut() {
      this.email = '';
      this.$emit('logOut');
    }
  }
}
</script>

<style scoped>

</style>