<template>
    <div>
        <a :href="link"><h1>{{nome}}</h1> <span><i class="devicon-doctrine-plain"></i></span></a>
    </div>
</template>
<script>
export default {
    props:['nome', 'link']
}
</script>
<style lang="scss" scoped>
    a{
        position:fixed;
        width:100px;
        text-align: center;
        z-index:5;
        bottom:10px;
        //left:50%;
        //margin-left:-50px;
        right:30px;
        h1{
            display:inline-block;
            font-size:12px;
            color:#FFF;
            margin-top:-5px;
    text-transform: uppercase;
        }
        span{
            overflow:hidden;
            width:23px;
            height:23px;
            display:inline-block;
            transform: rotate(90deg);
            border-radius: 50%;
            i{
                font-size:30px;
                color:#FFF;
                &::before{
                        margin-top: -8px;
                        display: block;
                        float:left;
                        margin-left: -4px;
                }
            }
        }
    }
</style>