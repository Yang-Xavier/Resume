<template>
    <div :class="className">
        <header class="clear-fix">
            <span class="fa fa-star"></span>
            <span>
                <h2>荣誉奖项</h2>
            </span>
        </header>
        <ul class="intro-content-2">
            <li>
                <h4>浙江省服务外包一等奖</h4>
            </li>
            <li>
                <h4>浙江省证券投资大赛量化组二等奖</h4>
            </li>
        </ul>
    </div>
</template>

<script>
    export default{
        name:'priceBlock',
        props:['className'],
        data(){
            return{

            }
        }
    }
</script>

<style></style>