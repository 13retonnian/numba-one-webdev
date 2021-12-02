<template>
  <div class="card text-center rounded-lg hover:shadow-2xl hover:text-purple-700">
    <a :href="info.account"><figure class="flex justify-center items-center flex-col">
      <div class="text-2xl p-5 font-bold" v-html="`<h3>${info.title}</h3>`"></div>
      <nuxt-img :src="info.image" sizes="sm:300px" />
      <figcaption v-text="info.description" />
      <img class="p-5" src="assets/images/gh-icon.png">
    </figure></a>
  </div>
</template>
<script>
export default {
  name: "Card",
  props: ["pageInfo", "info"],
};
</script>
<!-- CSS -->
<style>
.card {
  background: rgb(243, 243, 243);
  padding: 20px;
  width: 340px;
  justify-content: center;
}
figcaption {
  display: inline-block;
  padding-top: 1rem;
}
</style>
