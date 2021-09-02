<template>
  <div v-editable="blok" class="hero" :style="style">
    <div class="hero__text">
      <h1>{{ blok.header }}</h1>
      <p>{{ blok.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    blok: {
      type: Object,
      required: true,
    },
  },
  mounted() {
    console.log(this.blok)
  },
  methods: {},
  computed: {
    style() {
      return `background-image: url(${this.blok.image.filename})`
    },
  },
}
</script>

<style lang="scss" scoped>
.hero {
  width: 100%;
  height: 100vh;
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  position: relative;
  .hero__text {
    position: absolute;
    left: 70%;
    top: 40%;
    transform: translate(-70%, -40%);
    h1 {
      font-size: 40px;
      letter-spacing: 5px;
    }
    p {
      font-weight: 200;
      letter-spacing: 1.2px;
    }
    h1,
    p {
      margin: 0;
      padding: 0;
    }
  }
}
</style>