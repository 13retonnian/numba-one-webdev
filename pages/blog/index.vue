<template>
  <v-container>
    <h1 class="text-center">My Blog</h1>
    <ul>
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
