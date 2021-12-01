<template>
  <v-container>
    <h1 class="text-center p-5 text-5xl font-extrabold">Our Blog</h1>
    <ul class="flex flex-col bg-white h-screen rounded-r-lg p-10">
      <li
        class="bloglink p-5 hover:text-green-500"
        v-for="blog in blogs"
        :key="blog.id"
      >
        <NuxtLink class="text-2xl" :to="`blog/${blog.slug}`"
          ><strong>{{ blog.title }}</strong> -
          <em class="text-blue-500">"{{ blog.description }}"</em></NuxtLink
        >
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
<style>
.bloglink {
  text-shadow: 1px 1px 1px rgb(76, 76, 76);
}
</style>
