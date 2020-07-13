<template>
	<div>
		<div :class="comClass" @click="oclick">{{text}}</div>
	</div>
</template>

<script>
	export default {
		props:{
			text:{
				type:String,
				default:'确定'
			},
			comClass:{
				type:String,
				default:'com-class'
			}
		},
		data() {
			return {
				
			};
		},
		methods:{
			oclick(){
				const data = {
					tit:'点击'
				}
				this.$emit('hit',data)
			}
		}
	}
</script>

<style>
.com-class{
	height: 80rpx;
	line-height: 80rpx;
	background: #14BD79;
	color: #fff;
	font-size: 28rpx;
	width: 100%;
	text-align: center;
	border-radius: 8rpx;
}
</style>
