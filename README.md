# cpsc
移动端加载h5页面适配，实现swiper图片轮播使用任意尺寸手机屏幕，同时图片宽高也是可以任意指定，不采用@media()标签。

在浏览器模式下，加载的页面能够自由变换长宽而让页面保持适配，但是在移动端却会由于不同屏幕的宽高而出现问题。
本例实现再移动端加载h5页面，采用swiper控件实现图片轮播和手指触摸滑动效果。

难点：
由于移动端加载h5的时候获取的视口大小与完全渲染h5时获取的视口大小不一致，会导致swiper需要计算宽高问题不正确

解决方案：
通过onready、document.readyState="complete"都不奏效，采用计时器延缓计算swiper高度
