<template>
  <div class="card">
    <figure>
      <div v-html="`<h3>${info.title}</h3>`"></div>
      <nuxt-img :src="info.image" sizes="sm:300px" />
      <figcaption v-text="info.description" />
      <a href=""></a>
    </figure>
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
