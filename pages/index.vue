<template>
  <div class="flex h-screen w-screen bg-gray-200 relative" @click="touch()">
    <div class="m-auto text-6xl">{{ (elapsedTime / 1000).toFixed(3) }}</div>
    <svg
      class="h-10 w-10 absolute top-0 right-0 mt-2 mr-2"
      xmlns="http://www.w3.org/2000/svg"
      fill="none"
      viewBox="0 0 24 24"
      stroke="currentColor"
      @click.stop="info()"
    >
      <path
        stroke-linecap="round"
        stroke-linejoin="round"
        stroke-width="2"
        d="M13 16h-1v-4h-1m1-4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
      />
    </svg>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

const STATE = {
  wait: 'wait',
  running: 'running',
  stop: 'stop',
} as const

type State = typeof STATE[keyof typeof STATE]

type Data = {
  state: State
  startTime: number
  stopTime: number
  elapsedTime: number
  timerID: number
}

export default Vue.extend({
  name: 'App',
  data(): Data {
    return {
      state: STATE.wait,
      startTime: 0,
      stopTime: 0,
      elapsedTime: 0,
      timerID: 0,
    }
  },
  methods: {
    touch() {
      switch (this.state) {
        case STATE.wait:
          this.startTime = Date.now()
          this.timerID = window.setInterval(() => {
            this.elapsedTime = Date.now() - this.startTime
          }, 10)
          this.state = STATE.running
          break
        case STATE.running:
          this.stopTime = Date.now()
          clearInterval(this.timerID)
          this.elapsedTime = this.stopTime - this.startTime
          this.state = STATE.stop
          break
        case STATE.stop:
          this.elapsedTime = 0
          this.state = STATE.wait
          break
      }
    },
    info() {
      console.log('info')
    },
  },
})
</script>
