Tween.js

简介

各类缓动算法，效果演示参见：http://www.zhangxinxu.com/study/201612/how-to-use-tween-js.html

如何使用参见：http://www.zhangxinxu.com/wordpress/?p=5828

其中animation.js是新增，为了更简单的使用这些缓动算法，语法如下：

Math.animation(form, to, duration, easing, callback);
其中：

form和to是必须参数，表示动画起始数值和结束数值；
duration，easing，callback理论上都是可选参数，但是实际上callback肯定是要使用的，因为实时变化的数值就是通过callback返回的。然后，duration，easing，callback这3个参数的顺序是任意的。具体来讲：
duration为动画持续时间，默认300，默认单位是毫秒，建议使用数值，例如600，也支持带单位，例如600ms或者0.6s；
easing为缓动的类型，字符串类型，源自Tween.js。例如：'Linear'，'Quad.easeIn'，'Bounce.easeInOut'等等，需要注意大小写。 其中，默认值是'Linear'；
callback为回调函数，支持2个参数（value, isEnding），其中value表示实时变化的计算值，isEnding是布尔值，表示动画是否完全停止。
