<template>
<div>
  <Home />
  <About />
  <Portfolio />
  <Experiencia />
  <Footer />
  <!-- <Next :link="link" :nome="nome" /> -->
</div>
</template>

<script>
export default {
  data(){
    return{
      link: "#about",
      nome: "Sobre"
    }
  }
}
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;300;400;600;700;800;900&display=swap');
html {
   scroll-behavior: smooth;   
   overflow-x:hidden;
   font-family: 'Poppins', sans-serif;
   background:#080808;
}
</style>
