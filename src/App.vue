<template>
  <div id="app">
    <div style="display: flex; justify-content: center;">
      <router-view style="width: 70%;" />
    </div>

    <!-- Footer Starts from here -->

    <footer-component></footer-component>
  </div>
</template>

<script>
import footerComponent from "./components/footer.vue";
export default {
  components: { footerComponent },
  name: "App"
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
