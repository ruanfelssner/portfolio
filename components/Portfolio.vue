<template>
    
    <div id="portfolio" class="portfolio">
        <div class="container-fluid">
            <div class="row">
                <div class="container">
                    <div class="row mb-5">
                        <div class="col-12 text-center">
                            <h1 class="pt-5 pb-3">Projetos</h1>
                            <h5 class="px-5">Uma pequena galeria de projetos escolhidos por mim recentementes. Eu fiz tudo isso junto com pessoas incríveis por onde que passei. É apenas uma gota no oceano em comparação com toda a lista.</h5>
                        </div>
                    </div>
                    <div class="row">
                        <div v-for="(item, id) of computedObj" :key="id" class="col-12 col-md-4">
                            <div class="projeto" @click="index = id">
                                <span>{{item.nome}}</span>
                                <div class="recorte">
                                    <img :src="item.img" class="img-fluid" alt="">
                                </div>
                            </div>
                        </div>
                        <CoolLightBox :items="computedFotos" :index="index" @close="index = null" />
                    </div>
                    <div class="row justify-content-center align-items-center">
                        <div class="col-auto mb-5">
                            <button v-if="limit < portfolio.length" @click="limit=limit+3">+ Veja mais</button>
                            <button v-else @click="limit=3">Esconder</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import CoolLightBox from "vue-cool-lightbox";
import "vue-cool-lightbox/dist/vue-cool-lightbox.min.css";

export default {
    components: {
        CoolLightBox,
    },
    data(){
        return{
            portfolio: [],
            fotos: [],
            index: null,
            limit: 6
        }
    },
    computed:{
      computedObj(){
        return this.limit ? this.portfolio.slice(0,this.limit) : this.portfolio
      },
      computedFotos(){
        return this.limit ? this.fotos.slice(0,this.limit) : this.fotos
      }
    },
    mounted(){
        this.$axios.get('https://felss.dev/api/index.php?acao=portfolio', { progress: true }).then(res => {
            this.portfolio = res.data.map((res)=>{
                this.fotos.push('https://felss.dev/api/img/'+res.img)
                return {
                    ...res,
                    img: 'https://felss.dev/api/img/'+res.img
                }
            })
        })
    }
}
</script>
<style lang="scss" scoped>
.portfolio{
    background-color:#0b1e38;
  background: linear-gradient(132deg, #0b1e38, #10386f, #0b1e38);
  background-size: 200% 200%;
  animation: Gradient 15s ease infinite;
    min-height:100vh;
    z-index:2;
    position:relative;
    h1{
        margin-bottom:0;
        text-transform: uppercase;
        text-align: center;
        color:#FFF;
    }
    h5{
        color:#8c8c8c;
        font-weight: 200;
    }
    .projeto{
        &:hover{
            cursor:pointer;
            opacity:0.9;
        }
        span{
            text-transform: uppercase;
            font-size:12px;
            text-align: center;
            margin-bottom:10px;
            display:block;
            color:#FFF;
        }
        .recorte{
            max-height:170px;
            overflow:hidden;
            margin-bottom:40px;
            border-radius:10px;
            border:1px solid #383838;
            -webkit-box-shadow: 6px 7px 12px -1px rgba(0,0,0,0.21);
            -moz-box-shadow: 6px 7px 12px -1px rgba(0,0,0,0.21);
            box-shadow: 6px 7px 12px -1px rgba(0,0,0,0.21);
        }
    }
    button{
        text-transform: uppercase;
        font-weight: bold;
        background:#FFF;
        color:#0b1e38;
        border:0;
        border-radius:12px;
        padding:2px 10px;
        &:hover{
            opacity:0.9
        }
    }
}
</style>