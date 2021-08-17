<template>
    <div id="home" class="home container-fluid">
    <div class="row h-100 justify-content-center align-items-center">
      <div class="col-auto p-5">
        <h1>Olá, meu nome é Ruan Felssner.</h1>
        <p>Sou um desenvolvedor de web full-stack e estudante de Engenharia de Software.</p>
        <p>Confira meus artigos, componentes e projetos no Github.</p>
        <p>Sinta-se à vontade para dar uma olhada em meus projetos mais recentes abaixo.</p>        
        
      </div>
    </div>
    <Bubbles />
  </div>
</template>
<style lang="scss" scoped>
    @keyframes Gradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;300;400;600;700;800;900&display=swap');

.home{
  background-color:#10386f;
  background: linear-gradient(132deg, #0b1e38, #10386f, #0b1e38);
  background-size: 200% 200%;
  animation: Gradient .5s ease infinite;  
  background-size: 100% 100%;
  height:100vh;
  font-family: 'Poppins', sans-serif;
  transition: -webkit-transform 1.2s cubic-bezier(.165,.84,.44,1);
  transition: transform 1.2s cubic-bezier(.165,.84,.44,1);
  transition: transform 1.2s cubic-bezier(.165,.84,.44,1),
  -webkit-transform 1.2s cubic-bezier(.165,.84,.44,1);
    
  h1{
    color:#d4d4d4;
    font-weight:bold;
  }
  
  p{
    margin-bottom:5px;
    color:#8c8c8c;
    font-size:14px;
    padding-left:10%;
  }
  .row{
      z-index:2;
      position:relative;
  }
}
</style>