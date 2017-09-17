##多列布局
###定宽与自适应
	一、一列定宽一列自适应
 1、直接float:left;容易理解但是这样不够兼容。在IE6中文字有3像素的bug。
 2、改进方案：float + margin +（fix）
   这里.left要加个position：relative；来提高层级，不然会被right-fix的样式覆盖掉
   这种兼容性较高，虽然样式和结构写的比较多
 3、float + overflow
   出发BFC模式，但是在IE6还是不兼容
 4、table
   table默认宽度跟着内容走，设置宽度100%是希望他撑满父元素
   table-layout:fixed;作用：布局优先，加速table的渲染
 5、flex
   flex：1；相当于flex：1 1 0；即增长因子和收缩因子都为1，基础宽度为0
   flex除了不兼容低版本浏览器，还有性能较低，在小范围布局里使用较好，不适用于大范围布局。  