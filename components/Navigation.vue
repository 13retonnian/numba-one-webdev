<template>
  <v-container class="navlink">
    <ul class="font-bold flex pr-20">
      <li class="text-xl font-bold">
        <NuxtLink class="text-black hover:text-yellow-400 pr-5" to="/"
          >Home page</NuxtLink
        >
      </li>
      <li class="text-xl font-bold">
        <NuxtLink class="text-black hover:text-green-600 pr-5" to="/blog"
          >Blog</NuxtLink
        >
      </li>
      <li class="text-xl font-bold">
        <NuxtLink class="text-black hover:text-blue-500 pr-5" to="/team"
          >Our Team</NuxtLink
        >
      </li>
      <li class="text-xl font-bold">
        <NuxtLink class="text-black hover:text-purple-700 pr-5" to="/contact"
          >Contact</NuxtLink
        >
      </li>
    </ul>
  </v-container>
</template>

<script>
export default {};
</script>
