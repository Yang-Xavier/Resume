<template>
    <div>
        <div v-on:click="c">
            {{hello}}
        </div>
        <!--<transition name="line1" >-->
            <!--<div v-if="see" class="seep" :style="transition()"/>-->
        <!--</transition>-->
        <!--<transition name="line2" >-->
            <!--<div v-if="see" class="seep"/>-->
        <!--</transition>-->

        <transition
                @bofore-enter="beforeEnter"
                @enter="enter"
                @after-enter="afterEnter"
                @before-leave="beforeLeave"
        >
            <div v-if="see" class="seep"/>
        </transition>
    </div>
</template>

<script>
    import TWEEN from 'tween.js'

    export default{
        name:'test',
        data(){
            return{
                hello:'let me see',
                see:false,
//                transition:"transition: all 1s 0.5s linear"
            }
        },
        components:{
            t:{
                template:`<transition name="line" :style="">
                            <div class="seep"/>
                          </transition>`
            }

        }
        ,
        methods:{
            transition:()=>{
                return "transition: all 1s 0.5s linear"
            }
            ,
            c:function(){
                this.see=!this.see;
            },
            beforeEnter:(el)=>{
//                console.log(el.style)

            }
            ,
            enter:(el,done)=>{

                el.style.transition="all 1s"

//                done();
//                console.log(123)
//                this.$nextTick(done)
                setTimeout(done,0);
            },
            afterEnter:(el)=>{

//                console.log(321)
//                console.log(el.style.transition,el.style.width)
                el.style.width="400px";
            },
            beforeLeave:(el)=>{
                el.style.width="0";
//                el.style.transition="all 0s"
            },
            test:()=> {

                var c = {x: 0}
                new TWEEN.Tween(c)
                    .to({x: 10})
                    .onUpdate(function() {
                        console.log(this.x)
                    })
                    .start()

                requestAnimationFrame(animate);

                function animate(time) {
                    requestAnimationFrame(animate);
                    TWEEN.update(time);
                }

//                var coords = {x: 0, y: 0};
//                var tween = new TWEEN.Tween(c)
//                    .to({x: 100}, 1000)
//                    .onUpdate(function () {
//                        console.log(this.x);
//                    })
//                    .start();
//
//                requestAnimationFrame(animate);
//
//                function animate(time) {
//                    requestAnimationFrame(animate);
//                    TWEEN.update(time);
//                }



            }


        }
        ,
        mounted(){
//            this.test();
        }
    }
</script>

<style>
    .seep{
        width:0;
        height: 2px;
        font-size: 15px;
        background-color: wheat;
        display: block;
        /*transition: all 1s linear;*/
    }
    .line1-enter,.line2-enter{
        width: 0;
    }
    .line1-enter-active{

    }
    .line2-enter-active{
        transition: all 1s 0.5s linear;
    }
    .line1-leave-active,.line2-leave-active{
        transition: all 0s;
        width: 0;
    }
</style>