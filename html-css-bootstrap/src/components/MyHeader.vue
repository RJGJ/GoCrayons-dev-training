<script setup lang="ts">
import HomeIcon from './svg/HomeIcon.vue'
import InboxIcon from './svg/InboxIcon.vue';
import ExploreIcon from './svg/ExploreIcon.vue';
import ActivityIcon from './svg/ActivityIcon.vue';
</script>

<template>
  <header>
    <nav class="navbar navbar-expand navbar-light border-bottom fixed-top">
      <div class="container-lg d-flex">
        <a href="/" class="navbar-brand">
          <img src="../assets/logo.png" alt="site logo" />
        </a>
        <div class="mx-auto">
          <form class="d-flex">
            <input
              class="form-control me-2 d-none d-sm-block"
              type="search"
              placeholder="Search"
              aria-label="Search"
            />
          </form>
        </div>

        <!-- nav -->
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
        <div class="collapse navbar-collapse flex-shrink-1" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#">
                <HomeIcon />
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">
                <InboxIcon />
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">
                <ExploreIcon />
              </a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">
                <ActivityIcon />
              </a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template>

<style scoped lang="scss">
.navbar-collapse {
  flex-basis: 0 !important;
  flex-grow: 0;
}

.navbar {
  background-color: white;
}
</style>