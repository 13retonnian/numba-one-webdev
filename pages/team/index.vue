<template>
  <div>
    <Header :pageInfo="siteInfo" />
    <header>
      <h1>{{ siteInfo.pageName }}</h1>
      <main class="grid-box">
        <Cards v-for="topic in topics" :key="topic.id" :info="topic" />
      </main>
    </header>
  </div>
</template>

<script>
export default {
  data() {
    return {
      siteInfo: {
        pageName: "Card Gallery",
        author: "numbaone",
      },
      topics: [
        {
          title: "I'm Icha",
          img: "images/icah.png",
        },
        {
          title: "I'm Chris",
          img: "images/chris.png",
        },
        {
          title: "I'm Filora",

          img: "images/filora.png",
        },
        {
          title: "I'm James",

          img: "images/james.png",
        },
      ],
    };
  },
};
</script>

<style>
body {
  background-color: white;
}
.grid-box {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
  text-align: center;
}
</style>
