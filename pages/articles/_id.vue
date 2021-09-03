<template>
  <div>
    <h1>{{ article.title }}</h1>
    <p>{{ article.description }}</p>
  </div>
</template>

<script>
export default {
  async asyncData({ params, $axios }) {
    const article = await $axios.$get('https://dev.to/api/articles/721780')
    return { article }
  }
}
</script>
