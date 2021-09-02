<template>
  <div class="page" v-editable="blok">
    <component
      v-for="blok in blok.body"
      :key="blok._uid"
      :blok="blok"
      :is="blok.component"
    ></component>
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
  methods: {},
  computed: {},
}
</script>

<style lang="scss" scoped>
</style>