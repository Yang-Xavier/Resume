<template>
    <div class="bodyContainer row center-block">
        <lefter-intro/>
        <right-intro/>
    </div>
</template>

<script>
    import leftIntro from './LeftIntro/LeftIntro.vue'
    import rightIntro from './RightIntro/RightIntro.vue'
    import $ from 'jquery'

    export default{
        name:'bodyContainer',
        components:{
            lefterIntro:leftIntro,
            rightIntro:rightIntro
        },
        mounted(){
                $('#leftPane').css({
                    height:$('#rightPane').height()+'px'
                })

//            a()

        }
    }
    function a(){
        var pdf = new jsPDF('p', 'pt', 'letter');


//        pdf.canvas.height = 72 * 11;
        pdf.canvas.width = 1000;

        html2pdf(document.body,pdf,function (pdf) {
            pdf.save();
        })
    }

    function html2pdf (html,pdf,callback) {
        var canvas = pdf.canvas;
        if (!canvas) {
            alert('jsPDF canvas plugin not installed');
            return;
        }
        canvas.pdf = pdf;
        pdf.annotations = {

            _nameMap : [],

            createAnnotation : function(href,bounds) {
                var x = pdf.context2d._wrapX(bounds.left);
                var y = pdf.context2d._wrapY(bounds.top);
                var page = pdf.context2d._page(bounds.top);
                var options;
                var index = href.indexOf('#');
                if (index >= 0) {
                    options = {
                        name : href.substring(index + 1)
                    };
                } else {
                    options = {
                        url : href
                    };
                }
                pdf.link(x, y, bounds.right - bounds.left, bounds.bottom - bounds.top, options);
            },

            setName : function(name,bounds) {
                var x = pdf.context2d._wrapX(bounds.left);
                var y = pdf.context2d._wrapY(bounds.top);
                var page = pdf.context2d._page(bounds.top);
                this._nameMap[name] = {
                    page : page,
                    x : x,
                    y : y
                };
            }

        };
        canvas.annotations = pdf.annotations;

        pdf.context2d._pageBreakAt = function(y) {
            this.pageBreaks.push(y);
        };

        pdf.context2d._gotoPage = function(pageOneBased) {
            while (pdf.internal.getNumberOfPages() < pageOneBased) {
                pdf.addPage();
            }
            pdf.setPage(pageOneBased);
        }

        if (typeof html === 'string') {
            // remove all scripts
            html = html.replace(/<script\b[^<]*(?:(?!<\/script>)<[^<]*)*<\/script>/gi, '');

            var iframe = document.createElement('iframe');
            //iframe.style.width = canvas.width;
            //iframe.src = "";
            //iframe.document.domain =
            document.body.appendChild(iframe);
            var doc;
            doc = iframe.contentDocument;
            if (doc == undefined || doc == null) {
                doc = iframe.contentWindow.document;
            }
            //iframe.setAttribute('style', 'position:absolute;right:0; top:0; bottom:0; height:100%; width:500px');

            doc.open();
            doc.write(html);
            doc.close();

            var promise = html2canvas(doc.body, {
                canvas : canvas,
                onrendered : function(canvas) {
                    if (callback) {
                        if (iframe) {
                            iframe.parentElement.removeChild(iframe);
                        }
                        callback(pdf);
                    }
                }
            });

        } else {
            var body = html;
            var promise = html2canvas(body, {
                canvas : canvas,
                onrendered : function(canvas) {
                    if (callback) {
                        if (iframe) {
                            iframe.parentElement.removeChild(iframe);
                        }
                        callback(pdf);
                    }
                }
            });
        }

    }

</script>

<style>
    body{
        background-color: #cecece !important;
    }
    .bodyContainer{
        width: 100%;
        min-width: 1000px;
        border: 1px solid #888888;
        box-shadow: 5px 5px 5px #888888;
        margin: 10px 0;
    }
    ul{
        list-style: none;
        padding: 0 1rem;
    }
    ul li{
        padding: 0;
    }
    /*清除浮动*/
    .clear-fix:after{
        content:".";display:block;height:0;clear:both;visibility:hidden
    }
    .clear-fix{overflow:hidden}
    @media (min-width: 768px) {
        .bodyContainer{
            width: 100%;
        }
    }
    @media (min-width: 992px) {
        .bodyContainer{
            width: 90%;
        }
    }
    @media (min-width: 1200px) {
        .bodyContainer{
            width: 85%;
        }
    }
</style>