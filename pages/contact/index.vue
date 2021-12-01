<template>
  <div>
    <h1> {{ contactInfo.title }} </h1>
    <section>
      <ul>
      <li>Contact Number: {{ contactInfo.number }}</li>
      <li>Address: {{ contactInfo.address }}</li>
      <li>E-mail: {{ contactInfo.email }}</li>
    </ul>
    </section>
    <section>
      <nuxt-content :document="contactInfo" />
    </section>   
  </div>
</template>

<script>
export default {
  data(){
    return {
     
  }
}
}            
</script>

<style>

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

