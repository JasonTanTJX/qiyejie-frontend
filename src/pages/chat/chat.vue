<template>
	<view>
		<view class="cu-chat">
			<view class="cu-item self">
				<view class="main">
					<view class="content bg-green shadow">
						<text>早上好！</text>
					</view>
				</view>
				<view class="cu-avatar radius" :style="{'background-image':me}"></view>
				<view class="date">10:23</view>
			</view>
			<!-- <view class="cu-info round">对方撤回一条消息!</view> -->
			<view class="cu-item">
				<view class="cu-avatar radius" :style="{'background-image':opposite}"></view>
				<view class="main">
					<view class="content shadow">
						<text>Jason早上好呀！</text>
					</view>
				</view>
				<view class="date "> 10:29</view>
			</view>
			<!-- <view class="cu-info">
				<text class="cuIcon-roundclosefill text-red "></text> 对方拒绝了你的消息
			</view> -->
			<!-- <view class="cu-info">
				对方开启了好友验证，你还不是他(她)的好友。请先发送好友验证请求，对方验证通过后，才能聊天。
				<text class="text-blue">发送好友验证</text>
			</view> -->
			<view class="cu-item self">
				<view class="main">
					<image src="http://icon.tanyang.asia/cor.jpeg" class="radius" mode="widthFix"></image>
				</view>
				<view class="cu-avatar radius" :style="{'background-image':me}"></view>
				<view class="date"> 10:35</view>
			</view>
			<!-- <view class="cu-item self">
				<view class="main">
					<view class="action text-bold text-grey">
						3"
					</view>
					<view class="content shadow">
						<text class="cuIcon-sound text-xxl padding-right-xl"> </text>
					</view>
				</view>
				<view class="cu-avatar radius" :style="{'background-image':me}"></view>
				<view class="date">13:23</view>
			</view> -->
			<view class="cu-item self">
				<view class="main">
					<!-- <view class="action">
						<text class="cuIcon-locationfill text-orange text-xxl"></text>
					</view> -->
					<view class="content shadow">
						我到公司门口啦~
					</view>
				</view>
				<view class="cu-avatar radius" :style="{'background-image':me}"></view>
				<view class="date">10:35</view>
			</view>
			<view class="cu-item">
				<view class="cu-avatar radius" :style="{'background-image':opposite}"></view>
				<view class="main">
					<view class="content shadow">
						好的，一会儿见~
					</view>
					<!-- <view class="action text-grey">
						<text class="cuIcon-warnfill text-red text-xxl"></text> <text class="text-sm margin-left-sm">翻译错误</text>
					</view> -->
				</view>
				<view class="date">10:38</view>
			</view>
      <view class="cu-item self">
				<view class="main">
					<!-- <view class="action">
						<text class="cuIcon-locationfill text-orange text-xxl"></text>
					</view> -->
					<view class="content shadow">
						等会儿我们对一下项目
					</view>
				</view>
				<view class="cu-avatar radius" :style="{'background-image':me}"></view>
				<view class="date">10:40</view>
			</view>
      <view class="cu-item">
				<view class="cu-avatar radius" :style="{'background-image':opposite}"></view>
				<view class="main">
					<view class="content shadow">
						我等下还有个别的会议要开呢
					</view>
					<!-- <view class="action text-grey">
						<text class="cuIcon-warnfill text-red text-xxl"></text> <text class="text-sm margin-left-sm">翻译错误</text>
					</view> -->
				</view>
				<view class="date">10:41</view>
			</view>
      <view class="cu-item self">
				<view class="main">
					<!-- <view class="action">
						<text class="cuIcon-locationfill text-orange text-xxl"></text>
					</view> -->
					<view class="content shadow">
						好的，那我们换个时间
					</view>
				</view>
				<view class="cu-avatar radius" :style="{'background-image':me}"></view>
				<view class="date">10:41</view>
			</view>
      <view class="cu-item">
				<view class="cu-avatar radius" :style="{'background-image':opposite}"></view>
				<view class="main">
					<view class="content shadow">
						OK
					</view>
					<!-- <view class="action text-grey">
						<text class="cuIcon-warnfill text-red text-xxl"></text> <text class="text-sm margin-left-sm">翻译错误</text>
					</view> -->
				</view>
				<view class="date">10:42</view>
			</view>
		</view>

		<view class="cu-bar foot input" :style="[{bottom:InputBottom+'px'}]">
			<view class="action">
				<text class="cuIcon-sound text-grey"></text>
			</view>
			<input class="solid-bottom" :adjust-position="false" :focus="false" maxlength="300" cursor-spacing="10"
			 @focus="InputFocus" @blur="InputBlur">
			<view class="action">
				<text class="cuIcon-emojifill text-grey"></text>
			</view>
			<button class="cu-btn bg-green shadow">发送</button>
		</view>

	</view>
</template>

<script>
	export default {
		data() {
			return {
				InputBottom: 0,
        me:'url(http://icon.tanyang.asia/me.jpeg)',
        opposite: 'url(http://icon.tanyang.asia/mingren.jpeg)'
			};
		},
		methods: {
			InputFocus(e) {
				this.InputBottom = e.detail.height
			},
			InputBlur(e) {
				this.InputBottom = 0
			}
		}
	}
</script>

<style>
page{
  padding-bottom: 100upx;
}
</style>
