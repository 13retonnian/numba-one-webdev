<template>
  <div>
    <h1>{{ this.about }}</h1>
    <p>Path: {{ $route.path }}</p>
  </div>
</template>
<script>
  export default {
    async asyncData({ params }) {
      const about = params.about
      return { about }
    },
  }
</script>