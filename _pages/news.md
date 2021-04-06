---
layout: archive
title: "Images"
permalink: /images/
author_profile: true

---

<!doctype html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <title>文本折叠测试</title>
    <style>
        .a-text { font-size: 20px;color: #b30000;cursor: pointer;}
        .a-text:hover { color: red;}
        .p1 {font-size: 16px;color: #0a001f;width: 500px;  }
        .p2 { font-size: 16px; color: #0a001f; width: 500px; display: none;  }
    </style>
</head>
<body>
<p class="p1">
    1.substring 方法
    定义和用法substring 方法用于提取字符串中介于两个指定下标之间的字符。
    语法stringObject.substring(start,stop)参数 描述start 必需。一个非负的整数，
    规定要提取的子串的第一个字符在 stringObject 中的位置。stop 可选。一个非负的整数，
    比要提取的子串的最后一个字符在 stringObject 中的位置多 1。如果省略该参数，那么返回的
    子串会一直到字符串的结尾。返回值一个新的字符串，该字符串值包含 stringObject 的一个子字符串，
    其内容是从 start 处到 stop-1 处的所有字符，其长度为 stop 减 start。说明substring 方法返回的子串包
    括 start 处的字符，但不包括 end 处的字符。如果 start 与 end 相等，那么该方法返回的就是一个空串（即长度
    为 0 的字符串）。
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
        var a = $("<a></a>").on('click', showText).addClass('a-text').text("【展开】");
        var b = $("<a></a>").on('click', showText).addClass('a-text').text("【折叠】");
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
</html>
