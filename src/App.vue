<template>
  <div>
    <div class="container">
      <div class="py-5">
        <app-header :funds="funds"></app-header>
      </div>
      <router-view></router-view>
    </div>
  </div>
</template>
<script>
import Header from "./components/Header";
export default {
  components: {
    appHeader: Header
  },
  created () {
    this.$store.dispatch("initStocks");
  },
  computed: {
    funds () {
      return this.$store.getters.funds;
    }
  }
};
</script>
<style>
body {
  padding: 30px;
}
</style>
