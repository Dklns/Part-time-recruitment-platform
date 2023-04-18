<template>
	<view class="rough-task-item">
		<view class="info">
			<view class="avatar">
				<img :src="task.avatarImgSrc" :alt="task.name">
				<view>{{task.name}}</view>
			</view>
			<view class="duration">
				<span>周期</span>
				{{task.duration}}
			</view>
			<view class="reward">
				<span>报酬</span>
				{{task.reward}}元
			</view>
			<view class="distance">
				<span>距离</span>
				{{task.distance}}
			</view>
		</view>
		<view class="content">
			<text>
				<span>描述：</span>
				{{task.content}}
			</text>
		</view>
	</view>
</template>

<script>
	export default {
		name:"RoughTaskPresentation",
		props: ["task"],
		data() {
			return {
				
			};
		}
	}
</script>

<style lang="scss">
	.rough-task-item {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		align-items: flex-start;
		margin: 10px;
		padding: 5px 10px;
		border: 2px solid #575757;
		border-radius: 20px;
		background-color: #fbd066;
		
		.info {
			width: 100%;
			display: flex;
			justify-content: space-around;
			align-items: center;
			gap:30px;
			font-size: 1.1rem;
			border-bottom: 2px solid grey;
			
			.avatar {
				display: flex;
				justify-content: center;
				align-items: center;
				flex-direction: column;
				color: #575757;
				
				img {
					width: 50px;
					height: 50px;
					border-radius: 50%;
					object-fit: cover;
				}
			}
			
			.duration {
				display: flex;
				flex: 1;
				flex-direction: column;
				gap: 10px;
			}
			
			.reward {
				display: flex;
				flex: 1;
				flex-direction: column;
				gap: 10px;
				color: red;
			}
			
			.distance {
				display: flex;
				flex: 1;
				flex-direction: column;
				gap: 10px;
				color: #6a6a6a
			}
		}
	
		.content {
			margin-top: 10px;
			
			span {
				font-size: 1rem;
			}
		}
	}
</style>