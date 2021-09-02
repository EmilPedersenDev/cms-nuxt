<template>
  <header>
    <nav>
      <img src="acorn.png" alt="acorn logo" />
      <ul>
        <li><nuxt-link to="/">Home</nuxt-link></li>
        <li><nuxt-link to="/about">About</nuxt-link></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: '',
  data() {
    return {}
  },
  methods: {},
  computed: {},
}
</script>

<style lang="scss" scoped>
header {
  width: 100%;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 2;
  nav {
    width: inherit;
    padding: 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    img {
      height: auto;
      width: 50px;
    }
    ul {
      display: flex;
      padding: 0;
      margin: 0;
      li {
        list-style-type: none;
        margin-right: 10px;
        a {
          text-decoration: none;
        }
      }
    }
  }
}
</style>