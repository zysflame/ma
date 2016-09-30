#CALayer与UIView的区别

###基础
- [CALayer的定义](http://www.jianshu.com/p/b51c484d9d8f)


- [CALayer的基础](http://www.jianshu.com/p/3328037b2ed2)

- [CALayer和UIView的关系网上摘取的](http://www.jianshu.com/p/6351116c2d19)

###自己的理解
- 1、UIView主要是用于视图在屏幕上的展示，CALayer是对UIView所要展示的渲染不会直接展示到屏幕上；
- 2、UIView可以响应用户的操作而Layer不可以；

### 网上的资料
- 1、每个UIView都有一个CALyer实例的图层属性，视图的职责就是创建和管理这些图层，其实真正显示的和用来做动画的是背后关联的图层，UIView仅仅是对他的一个封装，提供了一些类似于处理用户交互的具体功能的接口。其实，UIView更像是一个CALayer的管理器，访问它的有关绘图跟坐标的属性，其实底层都是在访问CALayer的属性
- 2、每个UIView内部都有一个CALayer在背后提供内容的绘制和显示，并且在UIView的尺寸样式都是由内部的Layer所提供的，相同的是两者都有树状层级结构，layer内部youSublayers，View内部有Subviews，但是，Layer比View多个AnchorPoint。
- 3、Layer内部维持着三份layer tree（图层树）分别是：presentLayer Tree（动画树）、modeLayer Tree（模型树）、Render Tree（渲染树），在做 iOS动画的时候，我们修改动画的属性，在动画的其实是 Layer 的 presentLayer的属性值,而最终展示在界面上的其实是提供 View的modelLayer
- 4、两者最明显的区别是 View可以接受并处理事件，而 Layer 不可以。
- 5、在View即将显示的时候，UIView会自动的把图层的delegate设置为自己，并提供了一个displayLayer：的实现。
- 6、CALyer是默认修改属性支持隐式动画








