<script setup lang="ts">

import faker from 'faker';


function randomAvatar() { return faker.image.avatar(); }
function randomUsername() { return faker.name.firstName() }

</script>
<template>
  <div class="mx-2">
    <div class="outer-circle d-block mx-auto">
      <div class="inner-circle">
        <img :src="randomAvatar()" :alt="randomUsername() + '\'s avatar'" class="img-fluid" />
      </div>
    </div>
    <p class="text-center mb-0">{{ randomUsername() }}</p>
  </div>
</template>

<style scoped lang="scss">
.my-container {
  display: inline;
}
.outer-circle {
  width: 60px;
  height: 60px;
  padding: 2px;
  background: linear-gradient(
    45deg,
    #f09433 0%,
    #e6683c 25%,
    #dc2743 50%,
    #cc2366 75%,
    #bc1888 100%
  );

  .inner-circle {
    padding: 2px;
    background-color: white;
  }

  &,
  * {
    border-radius: 50%;
  }
}
</style>