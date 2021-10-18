<script setup lang="ts">
import { ref, computed } from "vue";
import faker from 'faker';

// Icons
import ThreeDotsIcon from "./svg/ThreeDotsIcon.vue";
import ActivityIcon from "./svg/ActivityIcon.vue";
import InboxIcon from "./svg/InboxIcon.vue";
import CommentsIcon from "./svg/CommentsIcon.vue";
import BookMarkIcon from "./svg/BookmarkIcon.vue";
import SmileyIcon from "./svg/SmileyIcon.vue";


function randomName() {
  return faker.name.findName();
}

function randomComment() {
  return faker.random.words(Math.random() * 9);
}

function randomImage() {
  return faker.image.image();
}

</script>
<template>
  <div v-for="i in 20">
    <div class="post mt-3 border">
      <div class="name p-3 d-flex align-items-center">
        <img :src="faker.image.avatar()" class="img-fluid avatar rounded-circle" />
        <p class="ms-3 my-auto">
          <strong>{{ randomName() }}</strong>
        </p>
        <div class="ms-auto">
          <a href="#">
            <ThreeDotsIcon />
          </a>
        </div>
      </div>
      <img :src="randomImage()" class="img-fluid mb-3" />
      <div class="post-meta px-3">
        <div class="d-flex mb-3">
          <div class="me-2">
            <a href="#">
              <ActivityIcon />
            </a>
          </div>
          <div class="me-2">
            <a href="#">
              <CommentsIcon />
            </a>
          </div>
          <div class="me-2">
            <a href="#">
              <InboxIcon />
            </a>
          </div>
          <div class="ms-auto">
            <a href="#">
              <BookMarkIcon />
            </a>
          </div>
        </div>
        <!-- caption -->
        <div>
          <p>
            <strong>{{ randomName() }}</strong>
            {{ randomComment() }}
          </p>
        </div>
        <!-- meta -->
        <small class="text-muted">View all {{ Math.floor(Math.random() * (999 + 1)) }} comments</small>
        <br />
        <small>
          <strong>{{ randomName() }}</strong>
          <span>&nbsp;{{ randomComment() }}</span>
        </small>
        <br />
        <small>
          <strong>{{ randomName() }}</strong>
          <span>&nbsp;{{ randomComment() }}</span>
        </small>
        <br />
        <small class="text-muted">3 HOURS AGO</small>
      </div>

      <!-- comment field -->
      <form class="input-group py-2 border-top">
        <span class="input-group-text bg-transparent border-0">
          <SmileyIcon />
        </span>
        <input
          type="text"
          class="form-control border-0 bg-transparent"
          placeholder="Add a comment..."
          aria-label="Add a comment..."
          aria-describedby="basic-addon1"
        />
        <span class="input-group-text text-primary comment-post bg-transparent border-0">
          <strong>Post</strong>
        </span>
      </form>
    </div>
  </div>
</template>

<style scoped lang="scss">
.avatar {
  height: 32px;
  width: 32px;
}

a,
a:hover {
  text-decoration: none;
  color: inherit;
}

small {
  font-size: 12px;
}
</style>
