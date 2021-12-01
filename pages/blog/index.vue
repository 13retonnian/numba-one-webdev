<template>
  <v-container>
    <h1 class="text-center p-5 text-8xl">My Blog</h1>
    <ul class="text-center p-10">
      <li v-for="blog in blogs" :key="blog.id">
        <NuxtLink class="text-xl" :to="`blog/${blog.slug}`"><strong>{{ blog.title }}</strong> - {{ blog.description }} </NuxtLink>
      </li>
    </ul>
  </v-container>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const blogs = await $content("blog").fetch();
    return {
      blogs,
    };
  },
  head() {
    return {
      script: [
        { src: "https://identity.netlify.com/v1/netlify-identity-widget.js" },
      ],
    };
  },
  generate: {
    fallback: true,
  },
};
</script>
