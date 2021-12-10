<template>
    <img :src="url" alt="">
</template>

<script>

export default {
  name: "Card1",
  props: {
      url: String,
  }
};
</script>

<style lang="scss" scoped>
</style>
