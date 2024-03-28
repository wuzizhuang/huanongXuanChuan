<template>
	<view class="body" @click="change">
		<image class="picture" :src="albums[index].path" mode="heightFix"></image>
		<view class="title">
			{{albums[index].name}}
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				albums: [{
					path: '../../static/行政楼.jpg',
					name: '行政楼'
				},{
					path: '../../static/教三大草坪.jpg',
					name: '教三大草坪'
				},{
					path: '../../static/赏樱亭.jpg',
					name: '赏樱亭'
				},{
					path: '../../static/西南门.jpg',
					name: '西南门'
				}],
				index: 0
			}
		},
		methods: {
			change() {
				while(true) {
					var i = Math.floor(Math.random() * 4);
					if(i != this.index) {
						this.index = i;
						break;
					}
				}
			}
		}
	}
</script>

<style>
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
	.picture{
		position: absolute;
		width: 100%;
		height: 100%;
		object-fit: cover;
		left: 50%;
		transform: translateX(-50%);
	}
	.title{
		color: aliceblue;
		position: absolute;
		left: 20px;
		bottom: 20px;
		font-size: 12vw;
		font-family: 'ShouXie';
	}
</style>