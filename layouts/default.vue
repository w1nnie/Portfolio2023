<template>
  <div>
    <FixedBar />
    <Nuxt />
  </div>
</template>

<script>
export default {
  mounted() {
    this.$adobeFonts(document)
  },
}
</script>
