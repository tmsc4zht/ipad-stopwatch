<template>
  <div class="relative">
    <div>
      <div><h1>iPad stopwatch</h1></div>
      <div>
        <h2><a href="/credits.txt">Credits</a></h2>
      </div>
    </div>
    <nuxt-link to="/">
      <svg
        class="h-10 w-10 absolute top-0 right-0 mt-2 mr-2"
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M6 18L18 6M6 6l12 12"
        />
      </svg>
    </nuxt-link>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>
