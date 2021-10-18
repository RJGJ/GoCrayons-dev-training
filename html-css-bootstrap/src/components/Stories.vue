<script setup lang="ts">

import StoriesAvatar from './StoriesAvatar.vue'

</script>

<template>
  <div class="border stories p-3 d-flex">
    <StoriesAvatar v-for="s in 5" />
  </div>
</template>

<style scoped lang="scss">
.stories {
  background-color: white;
}
</style>
