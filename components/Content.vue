<template>
  <v-container class="flex justify-center align-center flex-col text-center pt-20 m-auto">
    <h1 class="text-4xl p-5">
      {{ contactInfo.name }}
    </h1>
    <p class="text-2xl pb-10">
      {{ contactInfo.email }}
    </p>
  </v-container>
</template>
<script>
export default {
  // eslint-disable-next-line vue/require-prop-types
  props: ['contactInfo']
}
</script>
