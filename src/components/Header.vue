<template>
  <div>
    <nav class="navbar navbar-expand-md navbar-light bg-light fixed-top py-4">
      <div class="container">
        <div class="navbar-header">
          <router-link to="/" class="navbar-brand">ARBITRAGE TRADER</router-link>
        </div>

        <div class="collapse navbar-collapse">
          <ul class="navbar-nav mr-auto">
            <router-link to="/portfolio" activeClass="active" tag="li" class="nav-item">
              <a class="nav-link">Portfolio</a>
            </router-link>
            <router-link to="/stocks" activeClass="active" tag="li" class="nav-item">
              <a class="nav-link">Stocks</a>
            </router-link>
          </ul>
          <ul class="nav navbar-nav navbar-right">
            <li class="nav-item">
              <a class="nav-link" href="#" @click="endDay">End Day</a>
            </li>
            <li
              class="dropdown nav-item"
              :class="{open: isDropdownOpen}"
              @click="isDropdownOpen = !isDropdownOpen"
            >
              <a
                href="#"
                class="dropdown-toggle nav-link"
                data-toggle="dropdown"
                role="button"
                aria-haspopup="true"
                aria-expanded="false"
              >
                Save & Load
                <span class="caret"></span>
              </a>
              <ul class="dropdown-menu">
                <li class="nav-item">
                  <a class="nav-link" href="#" @click="saveData">Save Data</a>
                </li>
                <li class="nav-item">
                  <a href="#" @click="loadData">Load Data</a>
                </li>
              </ul>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>
<script>
export default {
  props: ['funds']
};
</script>
<style scoped>
/* body {
  margin-top: 105px;
} */

.navbar-brand {
  color: rgb(218, 8, 8);
}
.navbar {
  box-shadow: 2px 2px 5px #fdfdfd;
  opacity: 0.9;
  background: rgb(255, 255, 255);
}
.navbar .nav-item {
  font-size: 1.4rem;
  padding-right: 1.4rem;
}
</style>
