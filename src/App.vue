<template>
  <div id="app">
    <div class="container">
      <app-header></app-header>
      <router-view />
    </div>
    <app-footer></app-footer>
  </div>
</template>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
} */
</style>
<script>
import header from "./components/Header";
import footer from "./components/Footer";

export default {
  components: {
    "app-header": header,
    "app-footer": footer
    // 'app-footer': footer
  }
};
</script>