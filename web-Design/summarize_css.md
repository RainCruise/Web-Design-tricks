# CSS

+ IDs are Unique, Classes are Not Unique (https://css-tricks.com/the-difference-between-id-and-class/)

+ 尽可能少用绝对定位, 否则调试和修改的时候很费劲

+ 水平居中的方法: (https://segmentfault.com/a/1190000003110179)

    + 常用行内元素为a/img/input/span 等,标签内的HTML文本也属于此类: 给父元素设置 text-align:center来实现的。

    + 常用块级元素为div/table/ul/dl/form/h1/p等。

        + 定宽块级元素:
            满足**定宽**和**块状**两个条件的元素是可以通过设置 "margin: ** auto" 来实现居中的。

        + 不定宽块级元素:

            + 加入 table 标签
            + 设置 display: inline 方法
                (改变块级元素的 dispaly 为 inline 类型,然后使用 text-align:center 来实现居中效果)
            + 设置 position:relative 和 left:50%;
                (通过给父元素设置 float, 然后给父元素设置 position: relative 和 left:50%,
                子元素设置 position:relative 和 left: -50% 来实现水平居中)

+ 垂直居中的方法: (https://www.qianduan.net/css-to-achieve-the-vertical-center-of-the-five-kinds-of-methods/)

    + 已知高度:
         position: relative + top: calc(50% - height/2)

    + 未知高度:
        + vertical-align + table
            (首先为父元素加上 display: table，为子元素加上 display: table-cell 来将它们变成表格的样式，再为子元素加上 vertical-align: middle)
        + 为父元素添加伪元素

        + transform
            ( position: relative;
              top: 50%;
              transform: translateY(-50%);
            )

        + flexbox : 几乎一切位置问题都可以用flexbox解决
            ( display: flex;
              flex-direction: column;
              justify-content: center;
            )


