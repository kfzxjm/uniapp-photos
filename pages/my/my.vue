<template>
	<view class="userLayout pagetBg">
		<view class="userInfo">
			<view class="avatar">
				<image src="/static/images/logo.png" mode="aspectFill"></image>
			</view>
			<view class="ip">192.168.1.1</view>
			<view class="address">广西南宁市兴宁区</view>
		</view>
		<view class="selection">
			<view class="list">
				<view class="row">
					<view class="left">
						<uni-icons type="heart-filled" size="20"></uni-icons>
						<view class="text">我的收藏</view>
					</view>
					<view class="right">
						<view class="text">10</view>
						<uni-icons type="right" size="15" ></uni-icons>
					</view>
				</view>
				<view class="row">
					<view class="left">
						<uni-icons type="download-filled" size="20"></uni-icons>
						<view class="text">我的下载</view>
					</view>
					<view class="right">
						<view class="text">20</view>
						<uni-icons type="right" size="15" ></uni-icons>
					</view>
				</view>
				<view class="row">
					<view class="left">
						<uni-icons type="star-filled" size="20"></uni-icons>
						<view class="text">我的评分</view>
					</view>
					<view class="right">
						<view class="text">30</view>
						<uni-icons type="right" size="15"></uni-icons>
					</view>
				</view>
				<!-- #ifdef MP-WEIXIN -->
				<view class="row">
					<view class="left">
						<uni-icons type="chatboxes-filled" size="20"></uni-icons>
						<view class="text">联系客服</view>
					</view>
					<view class="right">
						<uni-icons type="right" size="15"></uni-icons>
					</view>
					<button open-type="contact"></button>
				</view>
				<!-- #endif -->
			</view>
		</view>
		<view class="selection">
			<view class="list">
				<view class="row" >
					<view class="left">
						<uni-icons type="notification-filled" size="20" ></uni-icons>
						<view class="text">订阅更新</view>
					</view>
					<view class="right">
						<uni-icons type="right" size="15"></uni-icons>
					</view>
				</view>
				<view class="row" >
					<view class="left">
						<uni-icons type="flag-filled" size="20"></uni-icons>
						<view class="text">常见问题</view>
					</view>
					<view class="right">
						<uni-icons type="right" size="15"></uni-icons>
					</view>
				</view>
			</view>
		</view>
		
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

	.selection{
		width: 690rpx;
		margin: 50rpx auto;
		border: 1px solid #eee;
		border-radius: 10rpx;
		box-shadow: 0 0 30rpx rgba(0, 0, 0, 0.05);
		.list{
			.row{
				display: flex;
				justify-content: space-between;
				align-items: center;
				padding: 0 30rpx;
				height: 100rpx;
				border-bottom: 1px solid #eee;
				position: relative;
				&:last-child{
					border-bottom: 0;
				}
				:deep(){
					.uni-icons{
						color: $brand-theme-color !important;
					}
				}
				.left{
					left: 0;
					display: flex;
					align-items: center;
					.text{
						padding-left: 20rpx;
						color: #666;
					}
				}
				.right{
					align-items: center;
					display: flex;
					.text{
						font-size: 28rpx;
						color: #666;
					}
				}
				button{
					position: absolute;
					height: 100rpx;
					width: 100%;
					left:0;
					top:0;
					opacity: 0;
				}
			}
		}
	}
}
</style>
