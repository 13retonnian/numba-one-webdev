<template>
  <div>
    <Header :pageInfo="siteInfo" />
    <header>
      <div class="theones">
        <h1>{{ siteInfo.pageName }}</h1>
        <main class="flex justify-evenly gap-y-16 flex-wrap p-10">
          <Card
            :pageInfo="siteInfo"
            v-for="card in profiles"
            :key="card.id"
            :info="card"
          />
        </main>
      </div>
    </header>
  </div>
</template>

<script>
export default {
  data() {
    return {
      siteInfo: {
        pageName: "The Ones",
        author: "numbaone",
      },
      profiles: [
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
h1 {
  font-size: 3rem;
  font-weight: 800;
  text-align: center;
}
main {
  gap: 13px;
}
.theones {
  padding-top: 3rem;
}
</style>
