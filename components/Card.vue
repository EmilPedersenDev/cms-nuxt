<template>
  <div v-editable="blok" class="card">
    <div class="left">
      <img :src="blok.image.filename" alt="monstrera" />
    </div>
    <div class="right">
      <div class="right__wrapper">
        <span> {{ blok.label }} </span>
        <h2>{{ blok.title }}</h2>
        <p>{{ blok.text }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: '',
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
  computed: {},
}
</script>

<style lang="scss" scoped>
.card {
  width: 100%;
  display: flex;
  padding: 200px 100px;
  background: #f4f1f1;
  flex-wrap: wrap;
  .left,
  .right {
    flex: 1 1 100%;
    @media (min-width: 1100px) {
      flex: 1 1 0%;
    }
  }

  .right {
    display: flex;
    justify-content: center;
    align-items: center;
    .right__wrapper {
      width: 100%;
      max-width: 400px;
      h2 {
        margin: 0px 0px 20px;
      }
      span {
        letter-spacing: 2px;
        font-size: 12px;
        opacity: 0.8;
      }
      p {
        margin: 0;
        line-height: 1.5;
        letter-spacing: 1.2px;
        font-size: 13px;
        font-weight: 200;
        opacity: 0.6;
      }
    }
  }

  .left {
    display: flex;
    justify-content: center;
    align-items: center;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      max-height: 400px;
      max-width: 500px;
      box-shadow: 0px 7px 20px 0px rgba(0, 0, 0, 0.4);
    }
  }
}
</style>