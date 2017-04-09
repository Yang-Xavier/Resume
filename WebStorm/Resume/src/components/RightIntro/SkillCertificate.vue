<template>
    <div :class="className">
        <header class="clear-fix">
            <span class="fa fa-id-card"></span>
            <span>
                <h2>技能证书</h2>
            </span>
        </header>
        <ul class="intro-content-2">
            <li>
                <h4>英语四级证书</h4>
            </li>
            <li>
                <h4>Java二级证书</h4>
            </li>
            <li>
                <h4>机动车驾驶证</h4>
            </li>
        </ul>
    </div>
</template>

<script>
    export default{
        name:'skillCertificate',
        props:['className'],
        data(){
            return{

            }
        }
    }
</script>

<style></style>