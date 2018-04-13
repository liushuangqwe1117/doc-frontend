## 示例  

#### 示例1：论坛评论  
图片宽高：50px * 50px  

效果图：  
![](/css/images/sample1.png)

代码：  
```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>论坛内容</title>
	<style type="text/css">
		h2,p {
			margin: 0;
			padding:0;
		}
		span {
			color: rgb(195,195,195);
		}
		section {
			font-family:"华文黑体","Times New Roman",Georgia,Serif;
			width: 500px;
			font-size: 12px;
		}
		header {
			padding: 0px;
			border-bottom: 2px solid red;
			margin-bottom: 5px;
		}
		header h2 {
			font-weight: normal;
			display: inline-block;
			margin-right: 20px;
		}
		section > div:after,li:after {
			content: '';
			display: block;
			clear: both;
		}
		img {
			float: left;
		}
		section > div form,li > div {
			position: relative;
			display: block;
			margin: 0px;
			padding: 0px;
			margin-left: 55px;
		}
		div.content textarea {
			width: 440px;
			height: 60px;
		}
		div.content + div {
			position: relative;
		}
		div.content + div button {
			position: absolute;
			right: 0;
			background: rgb(46,126,203);
			color: white;
			border: none;
			border-radius: 2px;
		}
		ul {
			margin: 0;
			padding: 0;
		}
		ul li {
			list-style: none;
			border-top: 1px solid rgb(213,213,213);
			padding-top: 10px;
			margin-top: 10px;
		}
		div.reply p {
			display: inline-block;
		}
		div.reply a {
			text-decoration: none;
			color: blue;
		}
		div.reply span {
			position: absolute;
			right: 0;
		}
	</style>
</head>
<body>
<section>
	<header>
		<h2>评论</h2>
		<span>共有3条评论</span>
	</header>
	<div>
		<a href="#"><img src="images/avatar1.png"></a>
		<form action="/comment" method="post">
			<div class="content"><textarea placeholder="评论"></textarea></div>
			<div>
				<span><span>130</span>/140</span>
				<button type="submit">评论</button>
			</div>
		</form>
	</div>
	<ul>
		<li>
			<a href="#"><img src="images/avatar2.png"></a>
			<div class="reply">
				<p><a href="#">葵葵</a>：很好听哈~</p>
				<span>28秒前</span>
			</div>
		</li>
		<li>
			<a href="#"><img src="images/avatar3.png"></a>
			<div class="reply">
				<p><a href="#">雅阁</a>：很适合睡觉时候听,试试看~</p>
				<span>28秒前</span>
			</div>
		</li>
		<li>
			<a href="#"><img src="images/avatar4.png"></a>
			<div class="reply">
				<p><a href="#">海苔</a>：很适合睡觉时候听~</p>
				<span>28秒前</span>
			</div>
		</li>
	</ul>
</section>
</body>
</html>
```
