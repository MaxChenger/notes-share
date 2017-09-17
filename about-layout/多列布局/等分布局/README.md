##多列布局
###等分布局

 1、float
  不足：结构和样式的耦合性太高，即这里是四等分25%，如果要换成其他比例布局
  的话又得修改结构又得修改样式
  <div class="parent">
		<div class="column" style="background:pink;"><p>1</p></div>
		<div class="column" style="background:yellow;"><p>2</p></div>
		<div class="column" style="background:pink;"><p>3</p></div>
		<div class="column" style="background:yellow;"><p>4</p></div>
	</div>
	
 2、table
  table的宽度设置为100%了就无法再修改它的宽度了，所以在结构上往parent外面
  再套一个div，修改它外面的div的宽度就可以了
  <div class="parent-fix">
		<div class="parent">
			<div class="column" style="background:pink;"><p>1</p></div>
			<div class="column" style="background:yellow;"><p>2</p></div>
			<div class="column" style="background:pink;"><p>3</p></div>
			<div class="column" style="background:yellow;"><p>4</p></div>
		</div>
	</div>
  这里通过table-layout：fixed使得结构和样式解耦了！
  
  3、flex
   .column +.column{
		margin-left: 20px;
	} 选择第一个column之后的所有column