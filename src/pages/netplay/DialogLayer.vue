<template>
	<div class="page-layer pointer-events-through">
		<SceneMenu v-if="dialogManage.menu.show"></SceneMenu>
		<PersonalCenter v-if="dialogManage.personalCenter.show"></PersonalCenter>
		<Chat v-if="dialogManage.chat.show"></Chat>
		<GameSetting v-if="dialogManage.gameSetting.show"></GameSetting>
		<FriendRoom v-if="dialogManage.friendRoom.show"></FriendRoom>
		<RuleInfo v-if="dialogManage.ruleInfo.show"></RuleInfo>
		<SuePeace v-if="dialogManage.suePeace.show"></SuePeace>
		<GiveUp v-if="dialogManage.giveUp.show"></GiveUp>
		<SearchRoom v-if="dialogManage.searchRoom.show"></SearchRoom>
		<RoomInfo v-if="dialogManage.roomInfo.show"></RoomInfo>
		<Victory v-if="dialogManage.victory.show"></Victory>
		<Login v-if="dialogManage.login.show"></Login>
	</div>
</template>

<script>
	import store from '@/store'
	
	import SceneMenu from './dialog/Menu'
	import RoomInfo from './dialog/RoomInfo'
	import PlayerInfo from './dialog/PlayerInfo'
	import RuleInfo from './dialog/RuleInfo'
	import SuePeace from './dialog/SuePeace'
	import GiveUp from './dialog/GiveUp'
	import Chat from './dialog/Chat'
	import FriendRoom from './dialog/FriendRoom'
	import Login from './dialog/Login'
	import SearchRoom from './dialog/SearchRoom'
	import PersonalCenter from './dialog/PersonalCenter'
	import Victory from './dialog/Victory'
	import GameSetting from './dialog/GameSetting'

	export default {
		data() {
			return {
				dialogManage: null
			}
		},
		props: [],
		created: function() {
			let scene = store.net.scene;
			this.dialogManage = scene.dialogManage;
		},
		methods: {

		},
		components: {
			SceneMenu,
			RoomInfo,
			PlayerInfo,
			RuleInfo,
			SuePeace,
			GiveUp,
			Login,
			SearchRoom,
			PersonalCenter,
			Victory,
			Chat,
			FriendRoom,
			GameSetting
		}
	}
</script>

<style>

</style>