<template>
    <div id="leftPane" class="col-sm-3 col-xs-3 col-md-3 left-block">
        <head-img className="img-block center-block"/>
        <base-info className="base-info-block center-block " />
        <skill-rank className="skill-block center-block"/>
        <hobby-block className="hobby-block center-block"/>
    </div>
</template>

<script>

    import headImg from './HeadImg.vue'
    import baseInfo from './BaseInfo.vue'
    import skillRank from './SkillRank.vue'
    import hobbyBlock from './HobbyBlock.vue'


    export default{
        name:'leftIntro',
        components:{
            headImg:headImg,
            baseInfo:baseInfo,
            skillRank:skillRank,
            hobbyBlock:hobbyBlock
        },
        data(){
            return{

            }
        }
    }
</script>

<style>
    .left-block{
        background-color: rgb(37,70,101);
        height: 100%;
        /*border: 1px solid #666666;*/
    }
    .img-block{
        margin: 4rem auto;
        width: 180px;
        height: 250px;
    }
    .img-block img{
        width: 100%;
        height: 100%;
    }



    /*baseInfo*/
    .info-block,.skill-block{
        width: 100%;
        margin:4rem auto;
        text-align: start;
    }
    .base-info-block ul{
        list-style: none;
        width: 100%;
        display: block;
        padding: 0 0.3rem 0 0;

    }
    .base-info-block ul>li{
        display: block;
        font-size: 2.5rem;
        width: 100%;
        color: #fff;
        margin-top: 15px;
        line-height: 2.5rem;
    }
    .base-info-block{
        width: 100%;
        margin-top: 2rem;
        text-align: start;
    }
    .base-info-block ul{
        list-style: none;
        width: 100%;
        display: block;
        padding: 0 0.3rem 0 0;

    }

    .base-info-block ul>li span:nth-child(1){
        text-align: center;
        display: block;
        width: 4rem;
        float: left;
    }

    .base-info-block ul>li span:nth-child(2){
        display: block;
        float: left;
        font-family: 微软雅黑;
        font-size: 1.5rem;
    }

    .base-info-block ul,
    .skill-block ul,
    .hobby-block ul{
        list-style: none;
        width: 100%;
        display: block;
        padding: 0 0.3rem 0 0;

    }
    .base-info-block ul>li {
        font-size: 2.5rem;
    }
    .base-info-block ul>li,.skill-block ul>li{
        display: block;
        width: 100%;
        color: #fff;
        margin-top: 15px;
        line-height: 2.5rem;
        overflow: hidden;
    }
    /*skillRank*/
    .skill-block ul>li{
        font-size: 1.5rem;
        width: 100%;
        padding-left: 1rem;
        margin: 1rem auto;
    }

    /*hobbyBlock*/
    .hobby-block h1{
        padding: 0 0;
        margin: 0 0 2rem 1rem;
        color: #fff;
        font-size: 2.5rem;
        line-height: 3rem;
        text-align: start;
    }
    .hobby-block ul>li{
        display: block;
        float: left;
        overflow: hidden;
        width: 49%;
        color: #fff;
    }
    .hobby-block ul>li section{
        display: block;
        text-align: center;
        margin: 1rem 0;
    }
    .hobby-block ul>li section:nth-child(1){
        font-size:4rem;
        width: 100%;
    }
    .hobby-block ul>li section:nth-child(2){
        font-size: 1.5rem;
        margin: 2rem 0;
    }





</style>