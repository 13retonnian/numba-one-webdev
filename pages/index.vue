<template>
  <v-container>
    <Header />
    <NuxtLink :to="`blog/${blog.slug}`"> {{ blog.title }}</NuxtLink>
  </v-container>
</template>

<script>
export default {
  head() {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
    };
  },

  generate: {
    fallback: true
  },
}
</script>
