<template>
	<view class="userLayout">
		<view class="userInfo">
			<view class="avatar">
				<image src="/static/images/logo.png" mode="aspectFill"></image>
			</view>
			<view class="ip">1111</view>
			<view class="address">11111</view>
		</view>
		<view class="selection"></view>
		<view class="selection"></view>
		
	</view>
</template>

<script setup>
	
</script>

<style lang="scss">
.userLayout{
	.userInfo{
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
		padding: 50rpx 0;
		.avatar{
			width: 160rpx;
			height: 160rpx;
			border-radius: 50%;
			overflow: hidden;
			image{
				width: 100%;
				height: 100%;
				
			}
		}
		.ip{
			font-size: 44rpx;
			color: #333;
			padding: 20rpx 0 5rpx;
		}
		.address{
			font-size: 28rpx;
			color: #aaa;
		}
	}
}
</style>
