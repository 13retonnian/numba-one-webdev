<template>
  <v-main>
   <v-container>
     <h1> {{ blog.title }} </h1>
     <section>
       <ul>
       <li>Description: {{ blog.image }}</li>
       <li>Publish Date: {{ blog.date }}</li>
     </ul>
     </section>
     <section>
       <nuxt-content :document="blog" />
     </section>
   </v-container>
 </v-main>
</template>
<script>
export default {
   async asyncData({ $content, params, error }) {
    try {
      const blog = await $content(`blog/${params.slug}`).fetch()
      return {
        blog,
      }
    } catch (e) {
      error('No article found')
    }
  },
}
</script>