<template>
<div>
  <Header :pageInfo="siteInfo" />
  <header>
    <h1> {{ siteInfo.pageName }}</h1>
    <main class="grid-box">
      <Cards v-for="topic in topics" :key="topic.id" :info="topic" />
    </main>
  </header>
</div>
</template>

<script>
export default {
  data () {
    return {
      siteInfo: {
        pageName: "Card Gallery",
        author: "numbaone",
      },
      topics: [
        {
          title: "I'm",
          description: "Danger 5 meme",
          img: "images/chuckle.jpeg"
        },
        {
          title: "Too",
          description: "Danger 5 meme",
          img: "images/chuckle.jpeg"
        },
        {
          title: "Lazy",
          description: "Danger 5 meme",
          img: "images/chuckle.jpeg"
        },
        {
          title: "To",
          description: "Danger 5 meme",
          img: "images/chuckle.jpeg"
        },
        {
          title: "Find",
          description: "Danger 5 meme",
          img: "images/chuckle.jpeg"
        },
        {
          title: "Pictures",
          description: "Danger 5 meme",
          img: "images/chuckle.jpeg"
        }
        
      ]
    }
  }
}
</script>

<style>
  .grid-box {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 10px;    
    text-align: center;
  }

</style>
