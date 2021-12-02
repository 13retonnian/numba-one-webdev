<template>
  <div>
    <Header :pageInfo="siteInfo" />
    <header>
      <h1>{{ siteInfo.pageName }}</h1>
      <main class="grid-box">
        <Cards v-for="topic in topics" :key="topic.id" :info="topic" />
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
          title: "I'm Icah",
          img: "images/icah.png",
          account: "https://github.com/Icahpv"
        },
        {
          title: "I'm Chris",
          img: "images/chris.png",
          account: "https://github.com/13retonnian"
        },
        {
          title: "I'm Filora",
          img: "images/filora.png",
          account: "https://github.com/aeoyu"
        },
        {
          title: "I'm James",
          img: "images/james.png",
          account: "https://github.com/Archangel767"
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
