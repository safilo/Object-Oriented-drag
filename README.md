# Object-Oriented-drag
面向对象+观察者模式的拖拽 <br>
demo: http://wlqing.com/demo/oop-drag"
##event.js 
跨浏览器的事件处理程序

<strong> myBind </strong> : bind方法的兼容性问题解决方案,将其添加到Function的原型上 <br>
<pre><code>fn.myBind(context,parameters);</code></pre>
<strong> on </strong> : 订阅(绑定)系统内置事件或自定义事件的方法,兼容IE6~8 <br>
<pre><code>on(obj, event, fn);</code></pre>
<strong> run </strong> : 发布(执行)IE6~8系统内置事件,解决IE6~8系统内置事件执行顺序和事件对象的问题 <br>
<strong> selfRun </strong> : 发布自定义事件(对应系统内置事件的run方法) <br>
<strong> off </strong> :  移除系统内置事件或自定义事件的方法,兼容IE6~8 <br>
<pre><code>off(obj, event, fn);</code></pre>

##drag.js
面向对象拖拽框架
###drag.js中down,move,up三个方法都提供一个接口(分别如下)，便于扩展拖拽的其他功能
<pre><code>on(obj, "selfDragStart", fn);</code></pre>
<pre><code>on(obj, "selfDragging", fn);</code></pre>
<pre><code>on(obj, "selfDragEnd", fn);</code></pre>

##elastic-potential-energy.js
在拖拽上扩展的弹性势能运动方法 <br>
订阅拖拽发生时的一系列自定义事件，在mouseup时通过计算水平速度和竖直高度，让其进行左右碰撞和自由落体运动
