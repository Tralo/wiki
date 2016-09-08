Android包含三种动画: View Animation(补间), Drawable Animation(帧动画),Property Animation(Android3.0新引入)

View Animation:

基于View的渐变动画，它只改变View的绘制效果，而实际属性值未变。比如动画移动一个按钮位置，但按钮点击的实际位置仍未改变。在代码中定义动画，可以参考AnimationSet类和Animation的子类，可以在res/anim/文件夹中定义XML文件。


Drawable Animation:

加载一系列Drawable资源來创建动画，这种传统动画某种程度上就是创建不同图片序列，顺序播放，就像电影胶片。在代码中定义动画帧，使用AnimationDrawable类;XML文件能更简单的组成动画帧，在res/drawable文件夹，使用<animation-list>采用<item>來定义不同的帧，感觉只能设置的属性是动画间隔时间。


Property Animation:

动画的对象除了传统的View对象，还可以是Object对象，动画之后，Object对象的属性值被实实在在的改变了。Property animation能够通过改变View对象的实际属性來实现View动画。任何时候View属性的改变，View能自动调用invalidate()试试刷新。