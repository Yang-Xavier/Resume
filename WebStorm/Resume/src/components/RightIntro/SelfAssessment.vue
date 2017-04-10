<template>
    <div :class="className">
        <header class="clear-fix">
            <span class="fa fa-file"></span>
            <span>
                <h2>自我评价</h2>
            </span>
        </header>
        <article class="intro-content-3">
            <p>
                客观的来说，本人性格比较外向，擅长沟通、交流与团队合作，对新鲜事物充满好奇心，喜欢钻研新奇的技术，同时具有较强的学习和实践能力。
                工作中，态度认真严谨又不失幽默。生活中，爱好广泛，擅长各项常见的体育运动。
            </p>
        </article>
    </div>
</template>

<script>
    export default{
        name:'selfAssessment',
        props:['className'],
        data(){
            return{

            }
        }
    }
</script>

<style></style>