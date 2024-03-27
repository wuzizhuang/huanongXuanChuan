<template>
	<view class="body">
		<image class="background" src="https://ts1.cn.mm.bing.net/th/id/R-C.f072a1063aa9df0021c870a915ff159c?rik=e1mke3nG%2fMFyZg&riu=http%3a%2f%2fwww.cleanpmp.com%2fFileUpLoad%2fjsFile%2f637209110978792987_1.jpg&ehk=jCuhs8mBLDQn5p8JNkZZCBmFlFFojtLKOMLE4eIF69w%3d&risl=&pid=ImgRaw&r=0" 
			mode="heightFix"></image>
		<view class="content">
			<view class="school">
				华南农业大学
			</view>
			<view class="title">
				-校园风景-
			</view>
		</view>
		<view class="operations">
			<navigator url="../see/see">
				<view class="button">
					参观校园
				</view>
			</navigator> 
			<view class="button">
				校园文化
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: 'Hello'
			}
		},
		onLoad() {
		},
		created() {
			this.playBackgroundMusic();
		},
		methods: {
			playBackgroundMusic(){
				const audio = new Audio('../../static/校歌.mp3');
				audio.loop=true;
				audio.play();
			}
		}
	}
</script>

<style lang="scss" scoped>
@font-face {
	font-family: "ShouXie";
	src: url('../../static/AaKLYLDYWNon-CommercialUse.woff')format('woff'),
	url('../../static/AaKLYLDYWNon-CommercialUse.woff2')format('woff2');
}
.body{
	overflow: hidden;
	display: flex;
	justify-content: center;
}
.background{
	position: absolute;
	z-index: -1;
	width: 100%;
	height: 100%;
	object-fit: cover;
	left: 50%;
	transform: translateX(-50%);
}
.content{
	position: relative;
	color: #f5f5f5;
	padding-top: 80px;
	text-align: center;
	display: flex;
	justify-content: center;
	width: 100%;
	height: 20vw;
	background-color: rgba(10, 10, 10, 0.2);
	border-radius: 0 0 16px 16px;
}
.school {
	text-shadow: 1px 1px 2px rgba(10, 10, 10, 0.5);
	font-family: 'ShouXie';
	font-size: 8vw;
	animation: textAnimation 3s infinite alternate;
}
@keyframes textAnimation {
  0% { font-size: 8vw; }
  100% { font-size: 10vw; }
}
.title {
	position: absolute;
	bottom: 5px;
	font-family: 'ShouXie';
	font-size: 6vw;
}
.operations{
	color: #f5f5f5;
	position: absolute;
	display: flex;
	justify-content: space-between;
	width: 70vw;
	top: 80vw;
	font-size: 30px;
	font-family: 'ShouXie';
}
.button{
	display: flex;
	justify-content: center;
	align-items: center;
	background-color: #1e824add;
	width: 30vw;
	height: 30vw;
	border-radius: 50%;
	box-shadow: inset 0 0 15px rgba(200, 200, 200, 0.8);
}
</style>
