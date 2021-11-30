<template>
  <div class="container">
      <AppHeader />
      <Nuxt />
      <AppFooter />
  </div>
</template>

<script>

</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    font-family: Arial, Helvtica, sans-serif;
    font-size: 1rem;
    line-height: 1.6;
    background: #f4f4f4
  }

  a {
    color: #666;
    text-decoration: none;
  }

  ul {
    list-style: none;
  }

  .container {
    max-width: 800px;
    margin: 2rem auto;
    overflow: hidden;
  }

  html {
    background-image: url("static/assets/images/background-image2.jpg");
    background-repeat: no-repeat;		
    background-position: top;	
    background-size: cover;	
  }

  h1 {
    font-size: 30px;
  }
</style>