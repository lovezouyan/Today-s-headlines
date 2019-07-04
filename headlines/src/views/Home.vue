<template>
		<div>
			<header>
					<div style="width:100%;height:40px;padding-top:10px;">
						<div id="logo">
							<img src="../assets/logo_tj.jpg" style="height:100%;width: 90%;"/>
						</div>
						<div id="search_div">
							<span style="float: left;line-height:40px;">123</span>
							<input type="text" class="el-icon-search"placeholder="中国海警钓鱼岛巡警" style="height:96%;width:85%;text-indent: 1em;border:none;float: left;"/>
						</div>
					</div>
					<div class="menu">
						<ul>
							<li>
								<a href="#">关注</a>
							</li>
							<li>
								<a href="#">推荐</a>
							</li>
							<li>
								<a href="#">热点</a>
							</li>
							<li>
								<a href="#">贵州</a>
							</li>
							<li>
								<a href="#">视频</a>
							</li>
							<li>
								<a href="#">图片</a>
							</li>
							<li>
								<a href="#">社会</a>
							</li>
						</ul>
					</div>
			</header>
			<nav>
				<div class="content_div">
					<ul>
						<list-news v-for="(item,index) in list" :key="index"> </list-news>
					</ul>
				</div>
			</nav>
			<footer>
				
				<bottompj v-for="(item,index) in list" :key="index"> </bottompj>
			
			</footer>
		</div>
</template>
<script>
	
	import ListNews from "../components/ListNews"
	
	import bottompj from "../components/bottompj"
	
	export default {
		name: "Home",
		
		components:{
			ListNews,
			bottompj
		},
		data(){
			return {
				list:[0,1,2,3,4],
			}
		}
	}


</script>
<style scoped lang="scss">
	#logo{
		float: left;
		width:30%;
		margin-left:2%;
		height:40px;
	}
	#search_div{
		float: left;
		margin-left:2%;
		width: 65%;
		height:40px;
		border-radius:5px;
		border:1px solid #ccc;
	}
	.menu{
		width:100%;
		text-align: center;
		height:35px;
		line-height:35px;
		border-bottom: 1px solid #CCCCCC;
	}
	.menu ul{
		list-style: none;
		padding-left: 0;
		magin-top:0;
	}
	.menu ul li{
		float: left;
		margin-left:2%;
		
	}
	.menu ul li a{
		display: block;
		font-size:16px;
		line-height:35px;
		font-weight:bold;
		color:#000;
		text-decoration: none
	}
	.menu ul li a:hover{
		border-bottom:2px solid red;
	}
	.content_div ul{
		list-style: none;
		padding-left: 0;
	
	}
	.content_div ul li{
		height:120px;
		width:100%;
		border-bottom: 1px solid #CCCCCC;
	}
	.content_div ul li .img_div{
		height:110px;
		width:25%;
		float: left;
		margin-left:2%;
		margin-top:10px;
	}
	.content_div ul li .text_div{
		float: right;
		height:110px;
		width:70%;
		
	}
	.title_div{
		text-align: left;
		text-indent:1em;
		font-size:18px;
		font-weight: bold;
		min-height:90px;
		overflow: hidden;
	}
	.bz_div{
		font-size: 12px;
		color:#444;
	}
	footer{
		position:fixed;
		bottom:0; 
		width:100%;
		border-top:1px solid #CCCCCC;
		height:60px;
		background: #fff;
	}
	.bottom_div{
		width:25%;
		float: left;
		font-size:14px;
	}
</style>
