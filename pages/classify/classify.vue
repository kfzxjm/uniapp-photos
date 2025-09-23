<template>
	<view class="classLayout">
		<view class="classify">
			<theme-item v-for="item in 18"></theme-item>
		</view>
	</view>
</template>

<script setup>

</script>

<style lang="scss">
	.classify{
		padding: 30rpx;
		display: grid;
		gap: 15rpx;
		grid-template-columns: repeat(3,1fr);
		
	}

</style>
