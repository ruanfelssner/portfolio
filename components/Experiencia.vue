<template>
    <div id="experiencia" class="experiencia">
        <div class="container-fluid">
            <div class="row">
                <div class="container py-5">
                    <div class="row mb-5">
                        <div class="col-12 text-center">
                            <h1>Experiência</h1>
                        </div>
                    </div>
                    <div class="row loopExp justify-content-center">
                        <div class="col-12 col-md-10">
                            <div v-for="(item, id) of experiencias" :key="id" class="row exp mb-4 mb-md-0" :class="item.posicao == 'right' ? 'justify-content-start' : 'justify-content-end'">
                        <div class="col-12 col-md text-right">
                            <div v-if="item.posicao == 'left'" class="card left">
                                <div class="data">
                                    <p>{{item.ano}}</p>
                                </div>
                                <h1>{{item.cargo}} - {{item.empresa}}</h1>
                                <p class="descricao">{{item.descricao}}</p>
                                <div class="vertical-timeline-element-content-arrow d-none d-md-block" :class="id == experiencias.length-1 ? 'bottom' : ''"></div>
                            </div>
                        </div>
                        <div class="d-none d-md-flex col-auto text-center justify-content-center" :class="id == experiencias.length-1 ? 'align-items-end' : 'align-items-start'">
                            <div class="circle d-flex justify-content-center align-items-center">
                                <i :class="item.icon"></i>
                            </div>
                        </div>
                        <div class="col-12 col-md text-left">
                            <div v-if="item.posicao == 'right'" class="card right">
                                <div class="data">
                                    <p>{{item.ano}}</p>
                                </div>
                                <h1>{{item.cargo}} - {{item.empresa}}</h1>
                                <p class="descricao">{{item.descricao}}</p>

                            <div class="vertical-timeline-element-content-arrow d-none d-md-block" :class="id == experiencias.length-1 ? 'bottom' : ''"></div>
                            </div>
                        </div>
                        <div class="linha d-none d-md-block"></div>
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
    data(){
        return {
            experiencias:[
              {
                    cargo: 'Engenheiro de software sênior',
                    empresa: 'Omint Saúde',
                    ano: '2022 - 2024',
                    descricao: 'Trabalhei nos projetos da Omint Saúde desenvolvendo o redesign dos aplicativos principais de associados, Kipp Saude, App Prestadores da Omint, Desenvolvimento de Frontend e seus padrões.',
                    posicao: 'left',
                    icon: 'devicon-devicon-plain'
                },
              {
                    cargo: 'Tech Lead',
                    empresa: 'Auzza Capital',
                    ano: '2022 - 2023',
                    descricao: 'Atuando na gestão de equipe de tecnologia, desenvolvimento de produto, regras de negócios e programando em Node.js (Backend) + Mysql e Mongodb + Nuxt.js e Next.js',
                    posicao: 'right',
                    icon: 'devicon-devicon-plain'
                },
                {
                    cargo: 'Fullstack',
                    empresa: 'AMA - Agentes do Meio Ambiente',
                    ano: '2019 - 2022',
                    descricao: 'Atualmente estou apoiando todos os setores no desenvolvimento dos produtos de software, desde o desenvolvimento de ferramentas para o mapeamento de microáreas, infraestrutura devops, requisitos de software e com o foco maior no desenvolvimento web de front e back end.',
                    posicao: 'left',
                    icon: 'devicon-devicon-plain'
                },
                {
                    cargo: 'Fullstack',
                    empresa: 'Agência Candy',
                    ano: '2013 - 2022',
                    descricao: 'Trabalhando com a parte Administrativa na gestão e com o desenvolvimento desde as partes gráficas como Photoshop, Illustrator, Premiere vetores logos cartões de visitas etc, como parte de front end, estruturação Bootstrap, UX UI, Wordpress, e parte de Programação em PHP, Ajax, Jquery, em sistemas personalizados aplicações de facebook, wireframes, integrações de sistemas e etc.Google analytics, Google Ads, Face Ads, Google Webmaster entre outras aplicações de divulgação e indexação.',
                    posicao: 'right',
                    icon: 'devicon-devicon-plain'
                },
                {
                    cargo: 'Front End',
                    empresa: 'Grupo Negócios Públicos',
                    ano: '2019',
                    descricao: 'Trabalhei no desenvolvimento web de seus produtos como ERP, Sollicita, Contract Vision, Compliance GOV, durante todo o período utilizei Sass, Razor do C#.net, participei de todo desenvolvimento do zero de alguns produtos como o Sollicita, Contract Vision, Compliance Criei alguns layouts e marcas do Contract Vision/Compliance, neste trabalho mesmo que o período pequeno as amizades continuam, equipe super enturmada, criamos um um bom vinculo mesmo após a saída.',
                    posicao: 'left',
                    icon: 'devicon-devicon-plain'
                },
                {
                    cargo: 'Fullstack',
                    empresa: 'Sites 10',
                    ano: '2014-2015',
                    descricao: "Exportação de Layouts em psd's para html/css/js e programação dos mesmos em php/mysql, paineis administrativos e gerenciaveis/ criação de ecommerce/ e etc.",
                    posicao: 'right',
                    icon: 'devicon-devicon-plain'
                },
                {
                    cargo: 'Front End',
                    empresa: 'Magic Web Design',
                    ano: '2013-2014',
                    descricao: 'Trabalho de atualizações de sites, portais, sistemas. Front end para sites de novos clientes, PSD, Html, Css, Jquery, clientes de grande porte tais como itau, sadia, yamaha etc.',
                    posicao: 'left',
                    icon: 'devicon-devicon-plain'
                },
                {
                    cargo: 'Auxiliar de Recursos Humanos',
                    empresa: 'Vaccinar',
                    ano: '2011-2013',
                    descricao: 'Como aprendiz trabalhei auxiliando todos os setores de RH, recrutamento e seleção, departamento pessoal e segurança no trabalho.',
                    posicao: 'right',
                    icon: ''
                },
            ]
        }
    }
}
</script>
<style lang="scss" scoped>
.experiencia{

  background-color:#080808;
    z-index:2;
    position:relative;
    h1{
        color:#FFF;
    }
    .loopExp{
        position:relative;
    }
    .exp{
        margin-bottom:0px;
        &:last-child{
            .circle{
                bottom:0;
            }
        }

        .linha{
            content: "";
            position: absolute;
            top: 0;
            left: 18px;
            height: 100%;
            width: 4px;
            background: #fff;
            left: 50%;
            margin-left: -2px;
            z-index:2;
        }
    }
    .card{
        position: relative;
        background: #fff;
        border-radius: .25em;
        padding: 1em;
        -webkit-box-shadow: 0 3px 0 #ddd;
        box-shadow: 0 3px 0 #ddd;
        h1{
            color:#080808;
        }
        &.left{
            // margin-left:60px;
            .vertical-timeline-element-content-arrow{
                left: 100%;
                -webkit-transform: rotate(180deg);
                transform: rotate(180deg);
            }
        }
        &.right{
            // margin-right:60px;
            .vertical-timeline-element-content-arrow{
                right: 100%;
            }
        }
        h1{
            font-size:14px;
            text-align: left;
        }
        p{
            font-size:10px;
            text-align:left;
            margin-bottom:0;
        }

    .vertical-timeline-element-content-arrow{
        content: "";
        position: absolute;
        top: 16px;
        height: 0;
        width: 0;
        border: 7px solid transparent;
        border-right-color: #fff;
        &.bottom{
            top:initial;
            bottom:16px;
        }
    }
    }
    .circle{
        width: 60px;
        height: 60px;
        border-radius: 50%;
        -webkit-box-shadow: 0 0 0 4px #fff, inset 0 2px 0 rgb(0 0 0 / 8%), 0 3px 0 4px rgb(0 0 0 / 5%);
        box-shadow: 0 0 0 4px #fff, inset 0 2px 0 rgb(0 0 0 / 8%), 0 3px 0 4px rgb(0 0 0 / 5%);
        background: #919191!important;
        color:#FFF;
        font-size:25px;
        z-index:3;
        position:relative;
    }
}
</style>
