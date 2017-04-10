<template>
    <div :class="className">
        <ul>
            <li>
                <section>html、css</section>
                <section >
                    <progress value="70" max="100"/>
                </section>
            </li>
            <li>
                <section>javascript</section>
                <section >
                    <progress value="70" max="100"/>
                </section>
            </li>
            <li>
                <section>java</section>
                <section >
                    <progress value="50" max="100"/>

                </section>
            </li>
            <li>
                <section>nodeJS</section>
                <section >
                    <progress value="50" max="100"/>

                </section>
            </li>
            <li>
                <section>ReactJS</section>
                <section >
                    <progress value="70" max="100"/>

                </section>
            </li>
            <li>
                <section>Vue</section>
                <section >
                    <progress value="60" max="100"/>

                </section>
            </li>
            <li>
                <section>PS</section>
                <section >
                    <progress value="50" max="100"/>

                </section>
            </li>
            <li>
                <section>项目管理、需求分析</section>
                <section >
                    <progress value="70" max="100"/>

                </section>
            </li>
        </ul>
    </div>
</template>

<script>
    export default{
        name:'skillRank',
        props:['className'],
        data () {
            return {

            }
        }

    }
</script>

<style>
    .skill-block ul>li .progress{
        height: 1rem;
    }
</style>