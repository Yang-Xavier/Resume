<template>
    <div :class="className">
        <img :src="img" class="img-thumbnail">
    </div>
</template>

<script>
    import logo from '../../assets/images/YBX.JPG'

    export default {

        name: 'headImg',
        props:['className'],
        data () {
            return {
                img:logo
            }
        }
    }
</script>

<style></style>