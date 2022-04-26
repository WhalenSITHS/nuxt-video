<template>
  <div>
    <h1>{{ article.title }}</h1>
    <nuxt-content :document="article" />
  </div>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const article = await $content('posts', params.slug).fetch()
    return { article }
  },
}
</script>

<style>
.nuxt-content {
  width: 80vw;
  margin: 2rem auto;
}
.nuxt-content h2 {
  color: red;
}
</style>
