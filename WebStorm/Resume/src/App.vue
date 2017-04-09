<template>
    <div>
        <body-container/>
    </div>
</template>

<script>
    import Container from './components/Container.vue'


    export default {

        name: 'app',
        data () {
            return {

            }
        },
        components:{
          bodyContainer:Container
        }
    }
</script>

<style>


</style>
