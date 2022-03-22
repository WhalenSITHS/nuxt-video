<template>
  <div>
    <h2>{{ title }}</h2>
    <p>{{ description }}</p>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      default: 'Title',
    },
    description: {
      type: String,
      default: 'Description',
    },
  },
}
</script>

<style></style>
