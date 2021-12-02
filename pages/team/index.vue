<template>
  <div>
    <Header :pageInfo="siteInfo" />
    <header>
      <h1>{{ siteInfo.pageName }}</h1>
      <main class="flex justify-evenly gap-x-16 gap-y-16 flex-wrap p-16">
        <Card
          :pageInfo="siteInfo"
          v-for="card in topics"
          :key="card.id"
          :info="card"
        />
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
          image: "assets/images/icah.png",
          title: "I'm Icha",
          description:
            "Aspiring pro front end developer. When I'm not in front of my computer, I enjoy hiking, walking my dog, having tea or coffee and eating chocolate. Trying to live life to the fullest!",
        },
        {
          image: "assets/images/chris.png",
          title: "I'm Chris",
          description: "",
        },
        {
          image: "assets/images/filora.png",
          title: "I'm Filora",
          description:
            "I strive for beautiful and functional designs. My current life motto is to learn and explore the possibilities of programming languages. ",
        },
        {
          image: "assets/images/james.png",
          title: "I'm James",
          description: "",
        },
      ],
    };
  },
};
</script>

<style>
body {
  /* background-color: white; */
}
.grid-box {
  /* display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-gap: 10px;
  text-align: center; */
}
.figcaption {
  margin: 0;
  display: inline-block;
}
</style>
