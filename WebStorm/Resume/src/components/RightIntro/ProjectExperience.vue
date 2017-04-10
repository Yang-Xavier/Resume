<template>
    <div :class="className">
        <header class="clear-fix">
            <span class="fa fa-clone"></span>
            <span>
                <h2>项目经验</h2>
            </span>
        </header>
        <ul class="intro-content-1">
            <li>
                <section class="clear-fix">
                    <span >
                        <p>
                            2017.04
                        </p>
                    </span>
                    <span>
                        <p>
                            全栈开发
                        </p>
                    </span>
                    <span>
                        <p>

                        </p>
                    </span>
                </section>
                <section>
                    <p>
                        全栈开发2017第一届手势控制主题Arduino创意开发大赛官网。前端使用Bootstrap框架+jQuery框架开发，后端使用nodeJS的Express框架进行开发，服务器使用Nginx，并配置服务器端口代理转发。
                        本次开发并未使用数据库，所有数据均存储为本地文件，为的是方便下载。
                    </p>
                    <p>
                        项目github链接 https://github.com/York-Bill/Competition-Hdumaker.git
                    </p>
                </section>
            </li>
            <li>
                <section class="clear-fix">
                    <span >
                        <p>
                            2016.10-2016.12
                        </p>
                    </span>
                    <span>
                        <p>项目管理、Web开发</p>
                    </span>
                </section>
                <section>
                    <p>
                        该项目主要为学校要求的开发任务，前端部分使用React框架进行开发，使用webpack打包代码，使用redux管理全局数据流。前后端分离开发，使用websocket和http请求进行数据交互。
                    </p>
                    <p>
                        前端部分github链接 https://github.com/SMG2/supermsg-web.git
                    </p>
                </section>
            </li>
            <li>
                <section class="clear-fix">
                    <span >
                        <p>
                            2016.07-2016.09
                        </p>
                    </span>
                    <span>
                        <p>Web开发、插件开发</p>
                    </span>
                </section>
                <section>
                    <p>
                        基于同花顺的量化交易平台，使用html编写界面，自学并使用lua语言编写网页控制脚本，实现MVC框架中的view和control，并调用同花顺提供的接口获取数据，完整的编写了一套智能交易策略，并获得二等奖。
                    </p>
                </section>
            </li>
            <li>
                <section class="clear-fix">
                    <span >
                        <p>
                            2016.04-2016.05
                        </p>
                    </span>
                    <span>
                        <p>项目管理、插件开发</p>
                    </span>
                </section>
                <section>
                    <p>
                        项目为服务外包命题，智能家居控制平台（手机APP），我主要负责项目管理，编写文档，制定开发计划，产品设计，使用java编写部分功能插件，以及硬件pcduino编程。并获得一等奖。
                    </p>
                </section>
            </li>
            <li>
                <section class="clear-fix">
                    <span>
                        <p>
                            2016.04
                        </p>
                    </span>
                    <span>
                        <p>Web开发</p>
                    </span>
                </section>
                <section>
                    <p>
                        参加杭州电子科技大学电子商务比赛，使用jQueryMobile框架+jQuery框架进行移动端Web页面开发，并获得三等奖。
                    </p>
                    <p>
                        项目github链接 https://github.com/York-Bill/JIE.git
                    </p>
                </section>
            </li>
            <li>
                <section class="clear-fix">
                    <span>
                        <p>
                            2014.12
                        </p>
                    </span>
                    <span>
                        <p>Web开发</p>
                    </span>
                </section>
                <section>
                    <p>
                        参加杭州电子科技大学软件工程学院软件嘉年华比赛，使用DIV+CSS+jQuery进行开发，制作一个简单的iPad模拟界面，并获得创意奖。
                    </p>
                </section>
            </li>
        </ul>
    </div>
</template>

<script>
    export default{
        name:'projectExperience',
        props:['className'],
        data(){
            return{

            }
        }
    }
</script>

<style></style>