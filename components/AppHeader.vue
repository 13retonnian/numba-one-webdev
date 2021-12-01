<template>
<div class="flex justify-between items-center flex-wrap">
  <header class="header p-10 text-center">
    <h1 class="title text-5xl font-extrabold overflow-hidden">NumbaOne</h1>
    <h2 class="text-2xl text-gray-500">Web Development</h2>
  </header>  
  <Navigation />
</div>
</template>

<script>
export default {
  name: 'AppHeader'
}
</script>
<!-- CSS -->
<style>

header {
  text-shadow: 1px 1px 2px black;
}

.header ul {
  display: flex;
}

.header a {
  display: inline-block;
  margin-right: 2rem;
  text-align: center;
  text-shadow: 1px 1px 1px rgb(79, 79, 79);
}
</style>