  页面布局的几种解决方案
  
#居中布局
###水平居中
  1、text-align + inline-block
    这种方法兼容性很好，缺点是子元素也会继承父元素的text-align:center;要让子元素的内容
	不会水平居中的话则需要另外设置
  
  2、table + margin
    这种需要设置子元素的display：table，这里容器的宽度是随着内容而变化的
	
  3、absolute + transform
    absolute的宽度由内容决定，left:50%;是使子容器的左边缘线对准父容器的中线
	另外translate是相对于自身的移动
   优点：absolute脱离文档流，子元素的移动不会影响其他元素
   确定：transform是css3的新内容，对IE678不兼容，而且在有些浏览器也需要加入一些前缀
   
  4、flex + justify-content
    子容器都为父容器的flex-items，且宽度是自适应内容的
	.parent{display: flex;justify-content:center;} 或者
    .parent{display: flex;} .child{margin:0 auto;}
	
###垂直居中
  1、table-cell + vertical-align
    使父容器变为一个单元格，设置单元格内容的位置
	
  2、absolute + transform
    同水平相同原理
   
  3、flex + align-items
    flex会让子容器默认高度为streach，即会拉伸为与父容器同样的高度
	所以要让它处在中间
	

###水平和垂直都居中
  1、inline-block + text-align +table-cell +vertical-align（思路是先水平后垂直）
    这种兼容性比较高
	
  2、absolute + transform
  
  3、flex +justify-content +align-items
 
  

   