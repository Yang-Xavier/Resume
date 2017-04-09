<template>
    <div :class="className">
        <ul>
            <li>
                <section>html、css</section>
                <section class="progress">
                    <div class="progress-bar " role="progressbar" aria-valuenow="100"
                         aria-valuemin="0" aria-valuemax="100" style="width: 60%;"
                    ></div>
                </section>
            </li>
            <li>
                <section>javascript</section>
                <section class="progress">
                    <div class="progress-bar " role="progressbar" aria-valuenow="100"
                         aria-valuemin="0" aria-valuemax="100" style="width: 70%;"
                    ></div>
                </section>
            </li>
            <li>
                <section>nodeJS</section>
                <section class="progress">
                    <div class="progress-bar " role="progressbar" aria-valuenow="100"
                         aria-valuemin="0" aria-valuemax="100" style="width: 40%;"
                    ></div>
                </section>
            </li>
            <li>
                <section>ReactJS</section>
                <section class="progress">
                    <div class="progress-bar " role="progressbar" aria-valuenow="100"
                         aria-valuemin="0" aria-valuemax="100" style="width: 60%;"
                    ></div>
                </section>
            </li>
            <li>
                <section>PS</section>
                <section class="progress">
                    <div class="progress-bar " role="progressbar" aria-valuenow="100"
                         aria-valuemin="0" aria-valuemax="100" style="width: 50%;"
                    ></div>
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