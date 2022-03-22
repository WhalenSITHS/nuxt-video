<template>
  <div>
    <Resource
      v-for="resource in resources"
      :key="resource.title"
      :title="resource.title"
      :description="resource.description"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      resources: [],
    }
  },
  async fetch() {
    this.resources = await this.$content('resources').fetch()
  },
}
</script>

<style scoped></style>
