<template>
    <div :class="className">
        <ul>
            <li class="clear-fix">
                <span class="fa fa-user"></span>
                <span>21岁</span>
            </li>
            <li class="clear-fix">
                <span class="fa fa-map-marker"></span>
                <span>浙江杭州</span>
            </li>
            <li class="clear-fix" >
                <span class="fa fa-phone-square"></span>
                <span>15096629921</span>
            </li>
            <li class="clear-fix">
                <span class="fa fa-envelope-open"></span>
                <span>xavier_ybx@163.com</span>
            </li>
            <li class="clear-fix">
                <span class="fa  fa-github-square"></span>
                <span>York-Bill</span>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {

        name: 'baseInfo',
        props:['className'],
        data () {
            return {

            }
        }
    }
</script>

<style>

</style>