<template>
  <v-main>
    <v-container>
      <h1>{{ siteInfo.title }}</h1>
      <section>
        <ul>
          <li>Image: {{ siteInfo.image }}</li>
          <li>Title: {{ siteInfo.title }}</li>
          <li>Description {{ siteInfo.description }}</li>
        </ul>
      </section>
      <section>
        <nuxt-content :document="siteInfo" />
      </section>
    </v-container>
  </v-main>
</template>
<script>
export default {
  props: ["siteInfo"],
};
</script>
