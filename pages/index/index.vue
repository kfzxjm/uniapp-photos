<template>
	<view class="homeLayout pagetBg">
		<view class="banner">
			<swiper indicator-dots circular autoplay indicator-color="rgba(255,255,255,0.5)" indicator-active-color="#fff">
				<!-- <swiper-item v-for="(img, index) in images" :key="index">
				  <image :src="img" mode="aspectFill" />
				</swiper-item> -->
				<swiper-item>
					<image src="/common/images/banner1.jpg"></image>
				</swiper-item>
				<swiper-item>
					<image src="/common/images/banner2.jpg"></image>
				</swiper-item>
				<swiper-item>
					<image src="/common/images/banner3.jpg"></image>
				</swiper-item>
			</swiper>
		</view>
		<view class="notice">
			<view class="left">
				<uni-icons type="sound-filled" size="20"></uni-icons>
				<text class="text">公告</text>
			</view>
			<view class="center">
				<swiper vertical autoplay interval="1500" duration="300" circular>
					<swiper-item >
						号外！号外！号外！号外！号外！号外！号外！号外！号外！号外！号外！号外！号外！号外！
					</swiper-item>
					<swiper-item>
						大新闻！大新闻！大新闻！大新闻！大新闻！大新闻！大新闻！大新闻！大新闻！大新闻！大新闻！
					</swiper-item>
				</swiper>
			</view>
			<view class="right">
				<uni-icons type="right" size="16"></uni-icons>
			</view>
			
		</view>
	
		<view class="select">
			<common-title>
				<template #title>每日推荐</template>
				<template #custom>
					<view class="date">
						<uni-icons type="calendar" size="30"></uni-icons>
						<view class="text">
							<uni-dateformat :date="Date.now()" format="yyyyMMdd"></uni-dateformat>
						</view>
					</view>
				</template>
			</common-title>
			<view class="content">
				<scroll-view scroll-x>
					<view class="box" v-for="item in 8">
						<image src="/common/images/preview_small.webp" mode="aspectFill"></image>
					</view>
				</scroll-view>
			</view>
		</view>
		
		<view class="theme">
			<common-title>
				<template #title>专题精选</template>
				<template #custom>
					<navigator url="" class="more">More+</navigator>
				</template>
			</common-title>
			<view class="content">
				<theme-item v-for="item in 8"></theme-item>
				<theme-item isMore=true></theme-item>
			</view>
	
		</view>
	</view>
</template>

<script setup>


</script>

<style lang="scss" scoped>
	.homeLayout{
		.banner{
			width: 750rpx;
			padding: 30rpx 0;
			swiper{
				height: 340rpx;
				width: 750rpx;
			
				swiper-item{
					width: 100%;
					height: 100%;
					padding: 0 30rpx;
					image{
						width: 100%;
						height: 100%;
						border-radius: 10rpx;
					}
				}
			}
		}
		.notice{
			width: 690rpx;
			height: 80rpx;
			background: #f9f9f9;
			margin: 0 auto;
			border-radius: 80rpx;
			display: flex;
			:deep(){
				.uni-icons{
					color: $brand-theme-color !important;
				}
			}
		
			.left{
				width: 140rpx;
				display: flex;
				align-items: center;
				justify-content: center;
				.text{
					color:$brand-theme-color;
					font-weight: 600;
					font-size: 28rpx;
				}
			
			}
			.center{
				flex: 1;
				swiper{
					height: 100%;
					swiper-item{
						display: flex;
						align-items: center;   /* 垂直居中 */
						justify-content: center; /* 水平居中 */
						height: 100%;
						font-size: 30rpx;
						color: #666;
						overflow: hidden;
						white-space: nowrap;
						text-overflow: ellipsis;
		
					}
				}

			}
			.right{
				width: 70rpx;
				display: flex;
				align-items: center;
				justify-content: center;
			}
		}
		
		.select{
			padding-top: 50rpx;
			:deep(){
				.uni-icons{
					color: $brand-theme-color !important;
				}
			}
			.content{
				width: 720rpx;
				margin-top: 30rpx;
				margin-left: 30rpx;
				scroll-view{
					white-space: nowrap;
					.box{
						width: 200rpx;
						height: 430rpx;
						margin-right: 15rpx;
						display: inline-block;
						image{
							width: 100%;
							height: 100%;
							border-radius: 10rpx;
						}
					}
					.box:last-child{
						margin-right: 30rpx;
					}
				}
			}
			.date{
				color: $brand-theme-color;
				align-items: center;
				display: flex;
				white-space: nowrap;
				.text{
					margin: left 15rpx;
				}
			}
			
		}
		
		.theme{
			padding: 50rpx 0rpx;
			.more{
				font-size: 32rpx;
				color: #888;
			}
			.content{
				margin-top: 30rpx;
				padding: 0 30rpx;
				display: grid;
				gap: 15rpx;
				grid-template-columns: repeat(3,1fr);
				
			}
		}
		
		
	}
	
</style>
