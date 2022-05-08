<template>
	<li @mouseenter="isHovering = true" @mouseleave="isHovering = false">
		<span>{{ label }}</span>
		<transition>
			<ul class="dropdown" v-show="isHovering">
				<li v-for="item in list" :key="item[0]">
					<nuxt-link :to="item[1]">{{ item[0] }}</nuxt-link>
				</li>
			</ul>
		</transition>
	</li>
</template>
<script>
export default {
	name: "Dropdown",
	props: {
		label: String,
		list: Array
	},
	data() {
		return {
			isHovering: false
		}
	}
}
</script>