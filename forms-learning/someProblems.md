 first-form.htnl:
     怎么调整fieldset的长度，现在是没有设置所以占满屏了好丑
	 (目前我是通过把表单包围在一个div里边然后给div设置宽度，可以解决这个问题)
	 
	 
	 
	 
	 
	 
	 
	 
	 
	 
	 
	 
包括：1、构建表单
	  2、提交给服务器处理
	  3、配置表单
	  4、表单验证
	  
	  
表单的elements集合是一个动态节点集合
  form.elements[i] 动态集合
  form[index] 静态集合  推荐使用
  
  
reset()
 可重置的元素:input,keygen,output,select,textarea
 触发表单reset事件，阻止该事件的默认行为可取消重置
 元素重置时不再触发元素上的change和input事件
 
label
 htmlFor：关联表单控件激活行为
		 可关联元素:button,input(hidden除外),keygen,meter,output,progress,select,textarea
   利用<label for="file">选择文件</label>	 可设置上传按钮效果
   for里的值是相应html的id值
   
 form：关联归属表单
	  可关联元素：button,fieldset,input,keygen,label,object,output,select,textarea
	  只读属性，不可在程序中修改
      可根据这个修改：label.setAttribute('form','newFormId');


input
   本地图片预览（有以下属性）	  
      onchange,accept,multiple,files