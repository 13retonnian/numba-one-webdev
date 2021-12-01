<template>
  <v-container>
    <h1>My Blog</h1>
    <ul>
      <li v-for="blog in blogs" :key="blog.slug">
        <NuxtLink :to="`blog/${blog.slug}`">{{ blog.title }}</NuxtLink>
        </li>
    </ul>
    
  </v-container>
</template>

<script>
export default {
   async asyncData({ $content, params }) {
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
