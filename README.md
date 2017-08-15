## learn_zepto
### 1.zepto和jquery异同点<br/>
　共同点:Zepto最初是为移动端开发的库，是jQuery的轻量级替代品，因为它的API和jQuery相似，而文件更小,Zepto所提供的工具足以满足开发程序的需要,如果熟悉jQuery，就能很容易掌握Zepto。你可用同样的方式重用jQuery中的很多方法，也可以方面地把方法串在一起得到更简洁的代码，甚至不用看它的文档.
  不同点:1.针对移动端程序2.Dom操作的区别：添加id时jQuery不会生效而Zepto会生效3.事件触发的区别4,事件委托的区别5.Zepto不支持的选择器等。
  整体结构
   ```javascript
  var Zepto = (function () {
    ...
  })()

  window.Zepto = Zepto
  window.$ === undefined && (window.$ = Zepto)
   ```
  如果在编辑器中将 zepto 的源码折叠起来，看到的就跟上面的代码一样。

  zepto 的核心是一个闭包，加载完毕后立即执行。然后暴露给全局变量 zepto ，如果 $ 没有定义，也将 $ 赋值为 zepto 。
