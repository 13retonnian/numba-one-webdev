<template>
  <v-main>
   <div class="bg-white flex flex-col justify-center items-center">
     <h1 class="p-10 italic shadow-md text-gray-700">" {{ blog.title }} " </h1>
     <section class="p-10 text-xl flex flex-col justify-center items-center">
       <ul>
        <li><img class="p-2 rounded-2xl" :src="blog.image" width="700" height="700"></li>
       <li class="p-2"><strong>Description:</strong> {{ blog.description }}</li>
       <li class="p-2"><strong>Publish Date:</strong> {{ blog.date }}</li>
     </ul>
     </section>
     <section class="content text-justify max-w-5xl leading-loose text-xl m-5">
       <nuxt-content :document="blog" />
     </section>
   </div>
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
<style>
h1 {
  font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  font-weight: bolder;
}

section {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  word-spacing: 5%;
}

a:hover {
  color: gray;
}

h2 {
  font-size: 2rem;
}

</style>