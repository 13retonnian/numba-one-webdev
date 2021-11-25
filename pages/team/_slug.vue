<template>
  <div>
    <h1>{{ this.team }}</h1>
    <p>Path: {{ $route.path }}</p>
  </div>
</template>
<script>
  export default {
    async asyncData({ params }) {
      const team = params.team
      return { team }
    },
  }
</script>