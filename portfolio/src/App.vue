<script setup>
// import TitlePage from "./components/TitlePage.vue";
// import Portfoilo from "./components/Portfoilo.vue";
// import About from "./components/About.vue";
import { RouterLink } from "vue-router";

import data from "./assets/portfolio.js";
</script>

<template>
  <nav
    class="navbar navbar-expand-lg bg-body-tertiary fixed-top"
    data-bs-theme="dark"
  >
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Navbar</a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <RouterLink class="nav-link active" aria-current="page" to="/"
              >Home</RouterLink
            >
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link" to="/portfolio">Portfolio</RouterLink>
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link" to="/about">About</RouterLink>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <router-view :data="data" />
</template>

<style scoped lang="scss"></style>
