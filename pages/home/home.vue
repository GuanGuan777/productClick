<template>
	<view class="page-wrapper">
		<view class="top-tab">
			<scroll-view scroll-x="true">
				<view class="tab-list">
					<view v-for="(tab,index) in tabs" :key="index" class="tab-item" :class="{'active': tabIndex==index}"
						@click="changeTab(index)">
						<view>
							{{tab.name}}
							<view class="tab-line"></view>
						</view>
					</view>
				</view>


			</scroll-view>
		</view>
		<view class="tabs-content">

			<view class="first-content" v-if="tabIndex==0">
				<view class="list">
					<view v-for="val in listData">
				
						<view class="list-content">
							<view class="title">{{val.title}}</view>
							<view class="content">{{val.content}}</view>
						</view>
				
					</view>
				</view>

			</view>
			<view class="second-content" v-if="tabIndex==1">
				<view>
					<view v-for="val in listData">

						<view class="list-content">
							<view class="title">{{val.title}}</view>
							<view class="content">{{val.content}}</view>
						</view>

					</view>
				</view>
			</view>
			<view class="third-content" v-if="tabIndex==2">7890</view>
		</view>

	</view>
</template>

<script>
	
	export default {
		data() {
			return {
				tabs: [{
					name: '业务1'
				}, {
					name: '业务2'
				}, {
					name: '业务3'
				}],
				tabIndex: 0,
				listData: [{
						title: '银企直连',
						content: '银行和企业最直接的服务连接'
					},
					{
						title: '银企直连',
						content: '银行和企业最直接的服务连接'
					},
					{
						title: '银企直连',
						content: '银行和企业最直接的服务连接'
					},
					{
						title: '银企直连',
						content: '银行和企业最直接的服务连接'
					},
					{
						title: '银企直连',
						content: '银行和企业最直接的服务连接'
					},
					{
						title: '银企直连',
						content: '银行和企业最直接的服务连接'
					},
					{
						title: '银企直连',
						content: '银行和企业最直接的服务连接'
					},
					{
						title: '银企直连',
						content: '银行和企业最直接的服务连接'
					},
					{
						title: '银企直连',
						content: '银行和企业最直接的服务连接'
					},
					{
						title: '银企直连',
						content: '银行和企业最直接的服务连接'
					},
					{
						title: '银企直连',
						content: '银行和企业最直接的服务连接的上的你你你你你你方法顶顶顶顶顶顶顶顶'
					},
					{
						title: '银企直连',
						content: '银行和企业最直接的服务连接'
					},
				],

			}
		},
		methods: {
			changeTab(index) {
				this.tabIndex = index
			}
		}
	}
</script>

<style lang="scss" scoped>
	.page-wrapper{
		background-color: #F2F6FA;
		-webkit-overflow-scrolling: touch;
	}
	.top-tab {

		width: 100%;
		height: 46px;
		font-size: 14px;
		background-color: #fff;
		.tab-list {
			display: flex;
			justify-content: space-around;
			height: 46px;
			align-items: center;
			.tab-item {
				flex: 1;
				text-align: center;
				position: relative;
				.tab-line {
					/* flex: 1;
				height: 2px;
				background-color: #007AFF; */
				}
			
			}
			.active{
				 .tab-line {
					/* flex: 1; */
					position: absolute;
					left: 50%;
					bottom: -12px;
					width: 33%;
					transform: translateX(-50%);
					height: 2px;
					background-color: #007AFF;
				}
				
			}
		}

	}

	
	.list-content {
		margin: 0 auto;
		width: 84%;
		background-color: #fff;
		margin-top: 16px;
		
		border-radius: 5px;
		padding: 16px;
		height: 80px;
		min-height: 80px;
		.title {
			color: #333;
			font-weight: 600;
			margin-bottom: 8px;
		
		}
		
		.content {
			color: #999;
			font-size: 12px;
		}
	}

	
</style>
