<template>
    <div :class="className">
        <header class="clear-fix">
            <span class="fa fa-fax"></span>
            <span>
                <h2>工作经历</h2>
            </span>
        </header>
        <ul class="intro-content-1">
            <li>
                <section class="clear-fix">
                    <span >
                        <p>
                            2014.09-2018.07
                        </p>
                    </span>
                    <span>
                        <p>杭州电子科技大学</p>
                    </span>
                    <span>
                        <p>本科</p>
                    </span>
                </section>
                <section>
                    <p>主修课程</p>
                    <p>
                        软件工程导论、数据结构、程序设计、计算机组成原理、操作系统
                        软件工程导论、数据结构、程序设计、计算机组成原理、操作系统
                        软件工程导论、数据结构、程序设计、计算机组成原理、操作系统
                        软件工程导论、数据结构、程序设计、计算机组成原理、操作系统
                    </p>
                </section>
            </li>
        </ul>
    </div>
</template>

<script>
    export default{
        name:'workExperience',
        props:['className'],
        data(){
            return{

            }
        }
    }
</script>

<style></style>