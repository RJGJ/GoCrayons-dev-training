<script setup lang="ts">

import faker from 'faker'

function randomAvatar() { return faker.image.avatar() }

function randomUsername() { return faker.internet.userName() }

function randomName() { return faker.name.findName() }

</script>

<template>
  <!-- Profile -->
  <div class="row my-3">
    <div class="col-3">
      <img :src="randomAvatar()" class="img-fluid rounded-circle" />
    </div>
    <div class="col-6">
      <strong>{{ randomUsername() }}</strong>
      <br />
      <small class="text-muted">{{ randomName() }}</small>
    </div>
    <div class="col-3">
      <button class="btn btn-sm text-primary">Switch</button>
    </div>
  </div>

  <!-- Suggestions -->
  <div class="row mb-3">
    <div class="col-8">
      <strong class="text-muted">Suugested For You</strong>
    </div>
    <div class="col-4">
      <button class="btn btn-sm p-0">See All</button>
    </div>
  </div>

  <div v-for="_ in 5" class="row mb-2">
    <div class="col-2">
      <img :src="randomAvatar()" class="img-fluid rounded-circle" />
    </div>
    <div class="col-6">
      <strong>{{ randomUsername() }}</strong>
      <br />
      <small class="text-muted">{{ randomName() }}</small>
    </div>
    <div class="col-4">
      <button class="btn btn-sm text-primary">Switch</button>
    </div>
  </div>

  <small>
    <ul class="breadcrumbs">
      <li>
        <a href="#">About</a>
      </li>
      <li>
        <a href="#">Help</a>
      </li>
      <li>
        <a href="#">Press</a>
      </li>
      <li>
        <a href="#">API</a>
      </li>
      <li>
        <a href="#">Jobs</a>
      </li>
      <li>
        <a href="#">Privacy</a>
      </li>
      <li>
        <a href="#">Terms</a>
      </li>
      <li>
        <a href="#">Locations</a>
      </li>
      <li>
        <a href="#">Top Accounts</a>
      </li>
      <li>
        <a href="#">Hashtags</a>
      </li>
      <li>
        <a href="#">Language</a>
      </li>
    </ul>
  </small>
</template>

<style scoped lang="scss">
.breadcrumbs {
  font-size: 12px;
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  padding: 0;
  list-style: none;

  a {
    text-decoration: none;
    padding-right: 5px;
    color: gray;
    transition: 250ms;

    &::before {
      content: "♦️ ";
    }

    &:hover {
      color: #0d6efd;
    }
  }
}
</style>