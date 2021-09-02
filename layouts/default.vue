<template>
  <div class="app">
    <e-header />
    <Nuxt />
    <e-footer />
  </div>
</template>

<script>
import Header from '../components/Header.vue'
import Footer from '../components/Footer.vue'
export default {
  components: {
    'e-header': Header,
    'e-footer': Footer,
  },
  data() {
    return {}
  },
  methods: {},
  computed: {},
}
</script>

<style lang="scss" scoped>
.app {
  position: relative;
}
</style>