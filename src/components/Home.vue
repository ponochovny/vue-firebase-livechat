<template>
	<div>
		<User>
			<template #user="{ user }">
				<div v-if="user">
					<UserProfile :user="user" />
					<ChatList :uid="user.uid" />
				</div>
				<Login v-else />
			</template>
		</User>
	</div>
</template>

<script>
import Login from './Login.vue'
import User from './User.vue'
import UserProfile from './UserProfile.vue'
import ChatList from './ChatList.vue'

export default {
	name: 'home-page',
	components: {
		Login,
		User,
		UserProfile,
		ChatList,
	},
}
</script>

<style></style>
