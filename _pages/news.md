---
layout: archive
title: "News"
permalink: /news/
author_profile: true

---

<head>
    <meta charset="UTF-8">
    <title>文本折叠测试</title>
    <style>
        .a-text { font-size: 20px;color: #b30000;cursor: pointer;}
        .a-text:hover { color: red;}
        .p1 {font-size: 16px;color: #0a001f; }
        .p2 { font-size: 16px; color: #0a001f;display: none;  }
    </style>
</head>
<body>
<p class="p1">
    <p>2021/Apr/1</p>
    Our first paper was published on The Journal of Clinical Investigation as a collaboration with The University of Michigan. Dr. Yoshida is the 1st co-first author and a co-corresponding autor. Two undergraduates, Wenyue Zheng and Rui Hua contributes thie as co-authors.<br>
    This paper was highlited as the cover article.<br>
</p>
</body>
<script src="https://cdn.bootcss.com/jquery/2.1.2/jquery.min.js"></script>
<script type="text/javascript">
    $(function () {
        text_foled('.p1', 100);
    });

    /**
     * jQuery 文本折叠展开特效
     * @param clas：存放文本的容器
     * @param num：要显示的字数
     */
   function text_foled(clas, num) {
        var num = num;
        var a = $("<a></a>").on('click', showText).addClass('a-text').text("[collapse]");
        var b = $("<a></a>").on('click', showText).addClass('a-text').text("[fold]");
        var p = $("<p></p>").addClass('p2');
        var str = $(clas).text();
        $(clas).after(p);
        if (str.length > num) {
            var text = str.substring(0, num) + "...";
            $(clas).html(text).append(a);
        }
        $('.p2').html(str).append(b);
        function showText() {
            $(this).parent().hide().siblings().show();
        }
    }
</script>
