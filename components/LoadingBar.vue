<template>
  <div id="loading-overlay" v-if="loading">
    <transition>
      <div class="loading-container">
        <img src="/Logo.jpg" alt="">
        <div class="bar"></div>
      </div>
    </transition>
  </div>
</template>
<script>
export default {
  data: () => ({
    loading: false
  }),
  methods: {
    start() {
      this.loading = true
    },
    finish() {
      this.loading = false
    }
  }
}
</script>