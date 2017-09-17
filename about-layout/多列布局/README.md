在“等高”的table方案中，使用padding-right的方案来处理间距会存在部分兼容问题。
问题表现：
在webkit和ie内核中会有这个问题，而firefox正常。从表现上看，似乎chrome等浏览器无故多
出了其他padding，如padding-bottom，从而导致了用background-clip:content-box来
裁剪背景后背景没有等高的问题。 

问题解决：
所以，为了解决这个兼容性问题，我们可以去掉padding-right的设置，变成
border-right:20px solid transparent，然后把background-clilp改成padding-box，问题就解决了。