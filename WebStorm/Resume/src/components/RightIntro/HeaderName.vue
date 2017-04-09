<template>
    <div :class="className">
        <h1>杨炳勋</h1>
        <h3 class="wanted">
            <span>求职目标：</span>
            <span>Web前端</span>
        </h3>
    </div>
</template>

<script>
    export default{
        name:'headerName',
        props:['className'],
        data(){
            return{

            }
        }
    }
</script>

<style></style>