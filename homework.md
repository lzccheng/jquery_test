## 1.原生js与jquery对象的互相转换方式分别有哪些,请举例说明

#### (1)、js 对象转jquery 对象
~~~ js
  var el = document.getElementById("box");
  var $el = $(el);
~~~
#### (2)、jquery 对象 转ｊｓ对象
~~~ js
  var $el = $('#box');
  var el = $el[0];
~~~
或者
~~~ js
 var $el = $('#box');
 var el = $el.get(0);
~~~

## 2.画图:jquery的ready事件和原生js的window.onload事件,在浏览器中的执行顺序
#### (1)、ＤＯＭ加载 --> $.ready()执行　--> css文件、js文件、图片、视频等文件加载　--> window.onload执行

## 3.如何将一个 HTML 元素添加到 DOM 树中的,写一段实例代码说明？
~~~ js
 var el = document.createElement('div');
 var $box = $('#box');
 $box.append(el);
 $box.prepend(el);
 $box.before(el);
 $box.after(el);
~~~

## 4.使用jQuery来提取一个HTML 标记的属性 例如. 链接的href, 写一段代码说明?
~~~ js
 var $a = $('#a');
 var value = $a.attr('href');
 $a.attr('href','https://www.baidu.com');
 $a.attr({'class':'aaa','id':'aaa'});
~~~

## 5.jQuery中 detach() 和 remove() 方法的区别是什么?
#### (1)、detach()移除本身和子元素，但元素上的jquery数据会保留
#### (2)、remove()移除本身和子元素，包括元素上的jquery数据以及绑定的事件,如果需要删除元素而不删除事件和jquery数据，则使用detach()。

## 6.如何利用jQuery来向一个元素中添加和移除CSS类?
~~~ js
 var $box = $('#box');
 $box.addClass('aaa');
 $box.removeClass('bbb');
 $box.toggleClass('ccc');
~~~

## 7.用jquery实现如下效果
#### [案例演示](http://book.jirengu.com/jirengu-inc/jrg-fe7/%E4%BD%9C%E4%B8%9A%E5%AE%89%E6%8E%92/jscode/JS8-jqery%E8%AF%AD%E6%B3%95/8-1.html)
#### [作品](./nav.html)

## 8.根据注释,使用jQuery为如下页面添加动画效果
~~~ js
 //元素：隐藏、 显示
 $('.box').hide('1000') //一秒时间去隐藏
 ('.box').show('4000')    //4秒去展示出来
 $('.box').toggle()     //切换
 $('.box').fadeIn()     //渐变，通过淡入的方式显示元素
  $('.box').fadeOut()     //淡出方式隐藏元素
  $('.box').fadeToggle()     //切换，展示的隐藏，隐藏的展示
  //元素： 滑动
  $('.box').slideDown()      //向下滑动动画显示一个匹配元素
  $('.box').slideUp()    //向上滑动
  $('.box').hide('slow')   //缓慢的隐藏匹配元素
~~~
## 9.使用 jQuery实现如下效果
#### [案例演示](http://demo.jb51.net/js/2014/jquery-tccdl-wsxqpzc/)
#### [作品](./header.html)

## 10.使用jQueryMobile 实现一个微信APP的简单一级菜单交互效果素材再发给大家
#### [作品](./wechat.html)
