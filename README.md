# cssDome

* div高度　由其内部文档流元素的高度总和决定

* 文档流　文档内元素的流动方向　
１．内联元素从左至右流动，满了，就换行（如果span有border，在流的过程被截断，会被分开，只有一个border。而hhaaaaaaaaaaaaaaaaaaaaaaaaa...作为一个整体，就不会分行，想要分行呢，添加work-break: break-all）
２．块级元素,从上往下，都另起一行

<hr>
* 内联元素的高度由什么确定，比如span的高度由什么决定？

预备：比如<span>你好a</span>,
基线，上部，下部。a与你好的基线对齐；
字体有建议的行高（比如上下两行字之间存在空隙）
你好
你好
这种形式；

* 实际上font-size设置的是，字体的最高点到最低点的大小；
比如span里有字，span的高度是由字体建议行高以及其它因素决定的 *

--------

* 给div指定height是引入bug的属性,不到情非得已千万不要指定高度.
* 块级元素的高度由其内部元素的高度总和决定。
* 脱离文档流：
1.position: fixed;　相对屏幕定位。
会产生问题，使用定位的元素会缩到左边去，解决办法：设置宽度100%，（不过这也是bug的来源)
会产生图１的问题，发现“其它”这两字已经快要出去了。
这个时候实际上由于刚才的宽度设置，导航条的宽度＋padding已经大于页面宽度。解决方法：
第一步，取消导航条的左右padding；效果如图２，发现效果还不好
第二步，添加一个div，包裹导航条。（同时注意清除浮动），给这个div设置左右padding就可以。如图３．

# icon全解
方法：
１．img法
２．background法
３．background合一法
４．font法
５．SVG法
６．新手慎用【CSS就是干】法
### img法
直接用img标签就可以。
好处：可以自适应，可以设置宽高。
### background法
用background背景图设置；
注意设置no-repeat；
好处，当div的宽高发生变化时，背景图不会随着它变化。
在css sprites（雪碧图）中应用，直接使用生成器就可以～
### icon-font
使用字体文件就可以。这个字体文件比较特殊是icon。
可以用html/css/js来分别实现

### SVG推荐使用
**优先使用symbol**
这三种的使用方法，查看iconfont
### css画，不推荐
参考：cssicon.space
