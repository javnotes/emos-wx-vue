<template>
	<view>
		<view>{{username}}</view>
		<view v-for="one in tel">{{one}}</view>
		<view v-if="age>=18">
			<button @tap="signUp()">报名按钮</button>
		</view>
		<view>
			<input type="text" v-model="address" placeholder="输入地址信息" />
		</view>
		<view>{{address}}</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				username: "Scott",
				tel: ["13312345678", "15912345678"],
				age: '20',
				address:"shanghai"
			}
		},
		methods: {
			signUp: function() {
				uni.showToast({
					title: "用户点击了报名按钮"
				})
			}

		}
	}
</script>

<style>

</style>
