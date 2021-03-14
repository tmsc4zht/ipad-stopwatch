<template>
  <div class="flex h-screen w-screen bg-gray-200">
    <div class="m-auto">{{ value }}</div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'App',
  data() {
    return {
      value: 'hello world',
    }
  },
})
</script>
