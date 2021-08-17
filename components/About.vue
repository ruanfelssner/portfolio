<template>
    <div id="about" class="about container-fluid">
        <div class="row h-100 justify-content-center align-items-center">
            <div class="container">
                <div class="row justify-content-center align-items-center">
                  <div class="col-8 col-md-3"><img src="../static/Ruan.jpg" class="w-100 p-2" /></div>
                  <div class="col-11 col-md">
                      <h1>Sobre mim</h1>
                      <p>Natural de Curitiba-PR, desde os 13 anos de idade se divertindo e trabalhando na área web, comecei desenvolvendo websites de jogos digitais e web rádios e até hoje estou aqui, aos 18 anos ingressei profissionalmente na área como Trainee, rápidamente consegui evolução e comecei minha jornada como Front-end.</p>
                      <p>Com 20 anos decidi buscar um novo desafio profissional e atuar como Fullstack onde aprendi muito. Em paralelo decidi empreender no meu próprio negócio, onde atuo até hoje. Aos 24 anos decidi focar em um sonho antigo de infância de desenvolver softwares e retornei ao mercado profíssional.</p>
                      <p>Hoje com {{(new Date().getFullYear())-1995}} anos, estudando Engenharia de Software na PUC-PR tenho como objetivo profissional alcançar grandes vôos e poder participar de grandes projetos.</p>
                  </div>
                </div>
                <hr />
                <div class="row habilidades d-none d-md-flex">
                    <div class="col-12">
                        <h5>Habilidades que conquistei</h5>
                        <div class="row">
                            <div v-for="(item, id) of habilidades" :key="id" class="col-1">
                                <div class="habilidade">
                                    <i :class="item.icon"></i>
                                    <span>{{item.nome}}</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
  </div>
</template>
<script>
export default {
    data () {
        return {
            habilidades:[
                { nome: 'Flask', icon: 'devicon-flask-plain'},
                { nome: 'Python', icon: 'devicon-python-plain'},
                { nome: 'Numpy', icon: 'devicon-numpy-plain'},
                { nome: 'Amazon', icon: 'devicon-amazonwebservices-original'},
                { nome: 'Docker', icon: 'devicon-docker-plain'},
                { nome: 'Jira', icon: 'devicon-jira-plain'},
                { nome: 'Trello', icon: 'devicon-trello-plain'},
                { nome: 'Heroku', icon: 'devicon-heroku-plain'},
                { nome: '.NET', icon: 'devicon-dotnetcore-plain'},
                { nome: 'C#', icon: 'devicon-csharp-plain'},
                { nome: 'Nuxt.js', icon: 'devicon-nuxtjs-plain'},
                { nome: 'Vue.js', icon: 'devicon-vuejs-plain'},
                { nome: 'Node.js', icon: 'devicon-nodejs-plain'},
                { nome: 'Express.js', icon: 'devicon-express-original'},
                { nome: 'Sequelize', icon: 'devicon-sequelize-plain'},
                { nome: 'Github', icon: 'devicon-github-plain'},
                { nome: 'Bitbucket', icon: 'devicon-bitbucket-plain'},
                { nome: 'Git', icon: 'devicon-git-plain'},
                { nome: 'Npm', icon: 'devicon-npm-original-wordmark'},
                { nome: 'Html', icon: 'devicon-html5-plain'},
                { nome: 'Apache', icon: 'devicon-apache-plain'},
                { nome: 'Vscode', icon: 'devicon-vscode-plain'},
                { nome: 'Css', icon: 'devicon-css3-plain'},
                { nome: 'Javascript', icon: 'devicon-javascript-plain'},
                { nome: 'Bootstrap', icon: 'devicon-bootstrap-plain'},
                { nome: 'Bulma', icon: 'devicon-bulma-plain'},
                { nome: 'Foundation', icon: 'devicon-foundation-plain'},
                { nome: 'Jquery', icon: 'devicon-jquery-plain'},
                { nome: 'Wordpress', icon: 'devicon-wordpress-plain'},
                { nome: 'Woo', icon: 'devicon-woocommerce-plain'},
                { nome: 'Ubuntu', icon: 'devicon-ubuntu-plain'},
                { nome: 'Filezilla', icon: 'devicon-filezilla-plain'},
                { nome: 'Putty', icon: 'devicon-putty-plain'},
                { nome: 'Figma', icon: 'devicon-figma-plain'},
                { nome: 'Photoshop', icon: 'devicon-photoshop-plain'},
                { nome: 'Illustrator', icon: 'devicon-illustrator-plain'},
                // { nome: 'xd', icon: 'devicon-xd-plain'},
            ]
        }
    }
}
</script>
<style lang="scss" scoped>

.about{
  background-color:#080808;
  background-image: url('../static/asfalt.png');
  background-size: 100% 100%;
  height:100vh;
  transition: -webkit-transform 1.2s cubic-bezier(.165,.84,.44,1);
  transition: transform 1.2s cubic-bezier(.165,.84,.44,1);
  transition: transform 1.2s cubic-bezier(.165,.84,.44,1),
  -webkit-transform 1.2s cubic-bezier(.165,.84,.44,1);
    z-index:2;
    position:relative;
  h1{
    color:#d4d4d4;
    font-weight:bold;
  }
  h5{
    color:#d4d4d4;
    font-weight:bold;
    margin:25px 0;
  }
  
  p{
    margin-bottom:5px;
    color:#8c8c8c;
    font-size:14px;
  }
  hr{
      background:#FFF;
      opacity:0.2;
      margin-top:30px;
  }
  img{
      border-radius:20px;
  }
  .habilidades{
      .habilidade{
          color:#FFF;
          margin-bottom:15px;
          text-align:center;
              margin-top:30px;
          i{
              font-size:30px;
          }
          span{
              clear:both;
              display:block;
              background:#FFF;
              color:#0b1e38;
              padding:0px 5px;
              text-transform: uppercase;
              font-size:10px;
              border-radius:12px;
          }
      }
  }
}
</style>