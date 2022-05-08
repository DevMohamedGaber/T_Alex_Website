<template>
	<div class="card-container">
		<div class="card">
			<div class="img" :style="{backgroundImage: `url(${data.img})`}"></div>
			<div class="info">
				<h2 v-if="data.title">{{ data.title }}</h2>
				<p v-if="data.info">{{ data.info }}</p>
			</div>
			<nuxt-link v-if="data.url" :to="data.url" class="more-btn">التفاصــيل</nuxt-link>
		</div>
	</div>
</template>
<script>
export default {
	props: {
		data: Object
	}
}
</script>