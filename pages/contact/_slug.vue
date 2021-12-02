<template>
  <v-main>
    <v-container>
      <h1>{{ contactInfo.title }}</h1>
      <section>
        <ul>
          <li>Contact Number: {{ contactInfo.number }}</li>
          <li>Address: {{ contactInfo.address }}</li>
          <li>Address: {{ contactInfo.address }}</li>
        </ul>
      </section>
      <section>
        <nuxt-content :document="contactInfo" />
      </section>
    </v-container>
  </v-main>
</template>
<script>
export default {
  props: ["contactInfo"],
};
</script>
