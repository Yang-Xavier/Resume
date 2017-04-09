<template>
    <div :class="className">
        <h1>兴趣爱好</h1>
        <ul>
            <li class="clear-fix">
                <section class="fa fa-globe"></section>
                <section>旅游</section>
            </li >
            <li class="clear-fix">
                <section class="icon-food"></section>
                <section>美食</section>
            </li>
            <li class="clear-fix">
                <section class="fa fa-camera"></section>
                <section>拍照</section>
            </li>
            <li class="clear-fix">
                <section class="icon-headphones"></section>
                <section>音乐</section>
            </li>
        </ul>
    </div>
</template>

<script>
    export default{
        name:'hobbyBlock',
        props:['className'],
        components:{},
        data(){
            return{

            }
        }
    }
</script>

<style></style>