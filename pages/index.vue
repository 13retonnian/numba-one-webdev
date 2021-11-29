<template>
  <v-container>
    <Header />
    <h1>My Blog</h1>
    <ul>
      <li>
        <NuxtLink :to="`blog/${blog.slug}`"> {{ blog.title }}</NuxtLink>
    </li>
    </ul>
    
  </v-container>
</template>

<script>
export default {
   async asyncData({ $content }) {
    const blogs = await $content('blog').fetch()
    return {
      blogs,
    }
  },
  head() {
    return {
      script: [
        { src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }],
    };
  },

  generate: {
    fallback: true
  },
}
</script>
