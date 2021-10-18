<script setup lang="ts">
import MyHeader from './components/MyHeader.vue';
import Stories from './components/Stories.vue';
import Posts from './components/Posts.vue'
import Sidebar from './components/Sidebar.vue';

// pseudo router


</script>

<template>
  <my-header></my-header>
  <main>
    <!-- feed -->
    <section class="bg-light pt-5" style="min-height: 100vh;">
      <div class="container py-4">
        <div class="row">
          <div class="col-lg-8 px-0">
            <Stories />
            <Posts />
          </div>
          <div class="col-lg-4">
            <div class="sticky-top" style="padding-top: 60px;">
              <Sidebar />
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>
