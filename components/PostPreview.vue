<template>
  <div class="PostPreview">
    <nuxt-link :to="{ name: 'slug', params: { slug: slug } }">
      Click ME</nuxt-link
    >
    <h3>{{ title }}</h3>
    <p>{{ desc }}</p>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Title',
    },
    desc: {
      type: String,
      default: 'Description',
    },
    slug: {
      type: String,
      default: '/',
    },
  },
}
</script>

<style>
.PostPreview {
  width: 40%;
  background-color: red;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  margin: 2rem auto;
  padding: 1rem;
}
</style>
