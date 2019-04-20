<template>
  <div>
    <div class="container">
      <div class="py-5">
        <app-header></app-header>
      </div>
      <div class="row">
        <div class="col-xs-12">
          <router-view></router-view>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Header from "./components/Header";
export default {
  components: {
    appHeader: Header
  }
};
</script>
<style>
body {
  padding: 30px;
}
</style>
