<template>
  <div id="app">
    <h1>Witaj w systemie zapisów na zajęcia</h1>
    <div v-if="!email">
      <login-form @login="logIn($event)" button-label="Zaloguj"></login-form>
    </div>
    <div v-else>
      <logged-in-form @logOut="logOut()" :email=email></logged-in-form>
    </div>
  </div>
</template>

<script>
import "milligram";
import LoginForm from "@/components/LoginForm";
import LoggedInForm from "@/components/LoggedInForm";

export default {
  components: {LoggedInForm, LoginForm},
  data() {
    return {
      email: '',
    }
  },
  methods: {
    logIn(username) {
      this.email = username;
    },
    logOut() {
      this.email = '';
    }
  }
}

</script>

<style>

</style>
