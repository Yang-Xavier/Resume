<template>
    <div id="rightPane" class="col-sm-9 col-xs-9 col-md-9 right-block">
        <header-name className="head-name-block info-block" />
        <education-block className=" info-block tittle-part"/>
        <schoole-experience className=" info-block tittle-part"/>
        <out-experience className=" info-block tittle-part"/>
        <work-experience className="info-block tittle-part"/>
        <project-experience className=" info-block tittle-part"/>
        <skill-certificate className=" info-block tittle-part"/>
        <price-block className=" info-block tittle-part"/>
        <self-assessment className=" info-block tittle-part"/>
    </div>
</template>

<script>
    import headerName from './HeaderName.vue'
    import educationBlock from './EducationBlock.vue'
    import skillCertificate from './SkillCertificate.vue'
    import schooleExperience from './SchoolExperience.vue'
    import outExperience from './OutExperience.vue'
    import workExperience from './WorkExperience.vue'
    import projectExperience from './ProjectExperience.vue'
    import priceBlock from './PriceBlock.vue'
    import selfAssessment from './SelfAssessment.vue'


    export default{
        name:'RightIntro',
        components:{
            headerName:headerName,
            educationBlock:educationBlock,
            skillCertificate:skillCertificate,
            schooleExperience:schooleExperience,
            outExperience:outExperience,
            workExperience:workExperience,
            projectExperience:projectExperience,
            priceBlock:priceBlock,
            selfAssessment:selfAssessment
        },
        data(){
            return{

            }
        }
    }
</script>

<style>
    .right-block{
        width: 100%;
        background-color: white;
    }
    .info-block{
        padding: 0 2rem;
        font-family: 微软雅黑;
        margin: 2rem 0;
    }
    .info-block h1{
        font-size: 5rem;
        padding: 0 0;
        margin: 0 0;
        color: rgb(37,70,101);
        line-height: 6.5rem;
        text-align: start;
    }
    .info-block h2{
        font-size: 3rem;
        padding: 0 0;
        margin: 0 0;
        color: rgb(37,70,101);
        line-height: 4rem;
        text-align: start;
    }
    .info-block h3{
        font-size: 2rem;
        padding: 0 0;
        margin: 0 0;
        color: rgb(37,70,101);
        line-height: 2.5rem;
        text-align: start;
    }
    .info-block h3.wanted{
        font-weight: 400;
    }
    .head-name-block{
        margin: 2rem 0;
        text-align: start;
    }

    .tittle-part header{
        width: 100%;
        color: rgb(37,70,101);
        display: block;
        height: 5rem;
    }
    .tittle-part header>span{
        float: left;
        line-height: 4rem;
    }
    .tittle-part header>span:nth-child(1){
        width: 4rem;
        font-size: 2.5rem;
        height: 4rem;
        text-align: center;
        border-radius: 8rem;
        background-color: rgb(37,70,101);
        color: #fff;
    }
    .tittle-part header>span:nth-child(2){
        width: calc(100% - 6rem);
        margin-left: 0.5rem;
        height: 4rem;
        vertical-align: top;
        border-bottom: 2px solid rgb(37,70,101);
    }

    .tittle-part .intro-content-1 li{
        /*background-color: #00AA88;*/
        padding: 1rem 0;
        text-align: start;
        word-break: break-all;
    }
    .tittle-part .intro-content-1 li section p{
        letter-spacing: 0.2rem;
        line-height: 2rem;
        margin: 0 0;
    }
    .tittle-part .intro-content-1 li section:nth-child(1) span{
        float: left;
        width: 30%;
        margin: 0 1%;
        font-size: 2rem;
    }
    .tittle-part .intro-content-1 li section:nth-child(2){
        margin: 1% 1%;
        width: 98%;
        font-size: 1.8rem;
    }

    .tittle-part .intro-content-2{
        padding: 0 3rem;
        list-style: disc;
    }
    .tittle-part .intro-content-2 li{
        /*background-color: #00AA88;*/
        padding: 1rem 0;
        text-align: start;
        word-break: break-all;
    }
    .tittle-part .intro-content-2 li h4{
        font-size: 2rem;
        margin: 0 0;
    }
    .tittle-part .intro-content-3{
        padding: 1rem 2rem;
        text-align: start;
        word-break: break-all;
        font-size: 1.8rem;
    }
    .tittle-part .intro-content-3 p{
        letter-spacing: 0.2rem;
        line-height: 2rem;
        margin: 0 0;
    }

</style>