<template>
  <div>
    <!-- Header Starts from Here  -->

    <header-component></header-component>

    <!-- Mid Content Starts From Here -->

    <div class="container-lg" style="display: flex; justify-content: center;">
      <router-view />
    </div>

    <!-- Footer Starts from here -->

    <footer-component></footer-component>
  </div>
</template>

<script>
import footerComponent from "./components/footer.vue";
import headerComponent from "./components/header.vue";
export default {
  components: { footerComponent, headerComponent },
  name: "App"
};
</script>

<style>
a {
  text-decoration: none;
}
</style>
