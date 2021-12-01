<template>
  <v-container>
    <h1 class="text-center">My Blog</h1>
    <ul>
      <li class="text-xl" v-for="blog in blogs" :key="blog.slug">
        <NuxtLink class="text-black hover:text-gray-400 drop-shadow-md" :to="`blog/${blog.slug}`"> <strong> {{ blog.title }} </strong> - {{ blog.description }}</NuxtLink>
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

