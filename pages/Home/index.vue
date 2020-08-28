<template>
	<view class="home-box">
		<view class="home-head">
			
			<view class="home-head-top">
				<text class="lg text-gray cuIcon-scan home-head-top-scan"></text>
				<text class="lg text-gray cuIcon-comment home-head-top-comment"></text>
			</view>
			
			<view class="home-head-card shadow-warp">
				<view class="home-head-input">
					<view class="home-head-input-icon">
						<text class="home-head-input-y">¥</text>
					</view>
					<view class="home-head-input-box">
						<input placeholder="请输入支付金额" value="2000.00" name="input" class="home-head-input-ipt"></input>
					</view>
				</view>
				<view class="home-head-card-btn-box">
					<button class="cu-btn round home-head-card-btn">
						<text class="lg text-gray cuIcon-qrcode home-head-card-qrcode">生成二维码 </text>
					</button>
				</view>
			</view>
		</view>
		
		<view class="home-menu">
			<view class="home-menu-box">
				<text class="lg text-gray cuIcon-qrcode home-menu-icon"></text>
				<text class="home-menu-title">生成二维码</text>
			</view>
			<view class="home-menu-box">
				<text class="lg text-gray cuIcon-scan home-menu-icon"></text>
				<text class="home-menu-title">扫码支付</text>
			</view>
			<view class="home-menu-box">
				<text class="lg text-gray cuIcon-card home-menu-icon"></text>
				<text class="home-menu-title">申请信用卡</text>
			</view>
			<view class="home-menu-box">
				<text class="lg text-gray cuIcon-redpacket home-menu-icon"></text>
				<text class="home-menu-title">积分兑换</text>
			</view>
		</view>
		
		
		<view class="home-plugs">
			<swiper class="screen-swiper round-dot" :indicator-dots="true" :circular="true"
			 :autoplay="true" interval="5000" duration="100">
				<swiper-item v-for="(item,index) in swiperList" :key="index">
					<image :src="item.url" mode="aspectFit" v-if="item.type=='image'"></image>
					<video :src="item.url" autoplay loop muted :show-play-btn="false" :controls="false" objectFit="cover" v-if="item.type=='video'"></video>
				</swiper-item>
			</swiper>
		</view>
		
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				dotStyle: false,
				swiperList: [{
					id: 0,
					type: 'image',
					url: 'http://livechb3.changhuoban.com/storage/images/e7ba544e88825ae17a0f3f77a4113c25.jpeg'
				}, {
					id: 1,
					type: 'image',
					url: 'http://livechb3.changhuoban.com/storage/images/6ba66275168b1508b6ff8dfff2982ed7.jpeg',
				}, {
					id: 2,
					type: 'image',
					url: 'http://livechb3.changhuoban.com/storage/images/c3cac14f81275dd1db68cfd60b7fcd58.png'
				}],
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
@import 'style/index.css';
</style>
