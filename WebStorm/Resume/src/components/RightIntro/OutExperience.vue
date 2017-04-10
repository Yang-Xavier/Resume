<template>
    <div :class="className">
        <header class="clear-fix">
            <span class="fa fa-suitcase"></span>
            <span>
                <h2>校外实践</h2>
            </span>
        </header>
        <ul class="intro-content-1">
            <li>
                <section class="clear-fix">
                    <span >
                        <p>
                            2016.09
                        </p>
                    </span>
                </section>
                <section>
                    <p>
                        参加G20峰会志愿服务，并获得志愿者服务证书以及优秀志愿者称号。
                    </p>
                </section>
            </li>
        </ul>
    </div>
</template>

<script>
    export default{
        name:'outExperience',
        props:['className'],
        data(){
            return{

            }
        }
    }
</script>

<style></style>