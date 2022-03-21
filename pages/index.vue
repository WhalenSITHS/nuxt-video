<template>
  <div>
    <PostPreview
      v-for="post in posts"
      :key="post"
      :title="post.title"
      :desc="post.description"
    ></PostPreview>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      posts: [],
    }
  },
  head() {
    return {
      title: `Blog`,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: `My beautiful blog`,
        },
      ],
    }
  },
  async fetch() {
    this.posts = await this.$content('posts').fetch()
  },
}
</script>
