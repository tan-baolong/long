<template>
	<view class="content">
		<view>
			<swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval">
				<swiper-item v-for="tupian in tupian" class="swiper-itpian">
					<image v-bind:src="tupian.zp"></image>
				</swiper-item>
			</swiper>
		</view>
		<view class="name">
			<p>石燕湖(4A)</p>
			<span>群山环抱，湖水清幽，天然大氧吧</span>
		</view>

		<view class="map">地址:湖南长沙雨花区跳马镇
			<a href='http://www.baidu.com'>地图></a>
		</view>

		<view style='height: 20upx;background-color: #f1f6f9;'></view>

		<view class="jdxx">
			<view class="jdxx-1">景点信息</view>
			<view class="jdxx-2">
				<span>优待政策</span>
				<p>
					70周岁（含）以上凭老年证或身份证免费，
					1.3米（含）以下半价，成人票九折
				</p>
			</view>
			<view class="jdxx-2">
				<span>开放时间</span>
				<p>
					全天08：30-17：00，16：30停止入场；
					夜场17：00-22：00，21：00停止入场
				</p>
			</view>
			<view class="jdxx-2">
				<span>景点简介</span>
				<p>
					湖南九寨人间瑶池,景区群山环绕<a href='#'>查看全部</a>
				</p>
			</view>
		</view>

		<view style='height: 20upx;background-color: #f1f6f9;'></view>

		<view class="mp">
			<view class="jdxx-1">门票</view>
			<ul>
				<li class="mp-1">
					<view style='width: 400upx;'>
						<p>[亲子票]1大1小+天空玻璃桥票+游玩项目套票</p>
						<p style="color: #58b2ef; font-size: 13px;margin-top: 10upx;margin-bottom: 10upx;">可订今日</p>
						<span class='sp'>官方</span>
						<span class='sp'>有条件退</span>
						<span class='sp'>无需换票</span>
						<view style='font-size: 14px;margin-top: 20upx;'>已售86 购买须知></view>
					</view>
					<view>
						<span style="color: #fe8e01;font-size: 20px;">￥412</span>
						<button style="border-radius: 80px;background:linear-gradient(#fd5d01,#fe8e01); color: #ffffff;">立即预定</button>
					</view>
				</li>
				<!-- <li class="mp-1"></li> A-->
			</ul>
		</view>

		<view style='height: 20upx;background-color: #f1f6f9;'></view>

		<view class="yhpj">
			<view class="jdxx-1">用户评价(6)</view>
			<!-- <ul> -->
			<uni-evaluate></uni-evaluate>
			<!-- </ul> -->
		</view>
	</view>
</template>

<script>
	import uniEvaluate from '../../components/xiujun-evaluate/uni-evaluate.vue'
	export default {
		data() {
			return {
				// indicatorDots: true,
				autoplay: false,
				interval: 2000,
				duration: 500,
				tupian: [{
						'id': 1,
						zp: '../../static/1.jpg'
					},
					{
						'id': 2,
						zp: '../../static/2.jpg'
					},
					{
						'id': 3,
						zp: '../../static/3.jpg'
					},
					{
						'id': 4,
						zp: '../../static/4.jpg'
					},
					{
						'id': 5,
						zp: '../../static/5.jpg'
					}
				]

			}
		},
		onLoad() {

		},
		methods: {

		},
		components: {
			uniEvaluate
		}

	}
</script>

<style>
	* {
		margin: 0upx;
		padding: 0upx;
	}

	.content {
		font-family: 楷体;
	}

	.swiper-itpian image {
		width: 750upx;
	}

	.swiper {
		height: 410upx;
		width: 750upx;
		background-size: 750upx 400upx;
		/* margin: 0upx auto; */
	}

	.name {
		height: 200upx;
		width: 700upx;
		margin: 0px auto;
		border-bottom: 2px solid #F7F9FA;
		/* line-height: 100upx; */
	}

	.name p {
		font-size: 23px;
		margin-bottom: 10upx;
	}

	.name span {
		font-size: 15px;
		color: #808080;
	}

	.map {
		font-size: 15px;
		height: 80upx;
		line-height: 80upx;
		width: 700upx;
		margin: 0px auto;
	}

	.map a {
		float: right;
	}

	.jdxx {
		width: 700upx;
		margin: 0px auto;
	}

	.jdxx-1 {
		border-bottom: 2px solid #F7F9FA;
		height: 80upx;
		line-height: 80upx;
	}

	.jdxx-2 {
		font-size: 15px;
		height: 100upx;
		border-bottom: 2px solid #F7F9FA;
	}

	.jdxx-2 span {
		color: #808080;
		width: 130upx;
		float: left;
		line-height: 40upx;
	}

	.jdxx-2 p {
		float: right;
		width: 530upx;
		line-height: 40upx;
		font-size: 13px;
	}

	.mp {
		width: 700upx;
		margin: 0px auto;
	}

	ul {
		list-style: none;
	}

	.yhpj {
		width: 700upx;
		margin: 0px auto;
	}

	.mp-2 {}

	.mp-1 {
		height: 250upx;
		/* background-color: #CCCCCC; */
		border-bottom: 2px solid #F7F9FA;

		font-size: 16px;
		margin-top: 20upx;
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
	}

	.sp {
		
		border: 1px solid #000000;
		font-size: 12px;
		/* fsiborder-radius: 4px; */
		margin-right: 10upx;
		padding: 5upx 10upx;
	}
</style>
