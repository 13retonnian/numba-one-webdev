<template>
  <div class="bg-white">
    <h1 class="text-center p-5"> {{ contactInfo.title }} </h1>
    <section class="text-center p-10 text-2xl">
      <ul>
      <li class="p-4"><strong>Contact Number:</strong> 
        {{ contactInfo.number }}</li>
      <li class="p-4"><strong>Address:</strong> 
        {{ contactInfo.address }}</li>
      <li class="p-4"><strong>E-mail:</strong> 
        {{ contactInfo.email }}</li>
      </ul>
    </section>
    <section>
      <nuxt-content :contactInfo="contactInfo" />
      <Content v-for="member in members" :key="member.id" :contactInfo="member"></Content>
    </section>   
  </div>
</template>
<script>
export default {
  data(){
    return {   
      contactInfo: {    
        title: "Contact Information",
        number: "555-555-5555",
        email: "NumbaOneWbdv@protonmail.com",
        address: "Moon Base Alpha, Moon, M0O 0N0",
      },
      members: [      
        {
          name: "Christopher Barber",
          email: "13retonnian@protonmail.com"
        },
        {
          name: "Icah Vega",
          email: "icah.doherty.vega@gmail.com"
        },
        {
          name: "James Atkinson",
          email: "jamesatkinson14@gmail.com"
        },
        {
          name: "Filora A",
          email: "filorat@outlook.com"
        }
      ],
  }
}
}            
</script>
