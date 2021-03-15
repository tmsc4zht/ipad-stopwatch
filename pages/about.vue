<template>
  <div class="relative">
    <!-- main content-->
    <div class="container mx-auto">
      <h1 class="text-2xl mb-2">iPad stopwatch</h1>
      <div class="mb-2">
        <h2 class="text-lg">About</h2>
        <p>A stopwatch click or tap to start, stop and reset.</p>
      </div>
      <div class="mb-2">
        <h2 class="text-lg">Auther</h2>
        <p>tmsc4zht(@tmsc4zht)</p>
      </div>
      <div class="mb-2">
        <h2 class="text-lg">Acknowledgements</h2>
        <p><a class="underline" href="/credits.txt">Credits</a></p>
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
