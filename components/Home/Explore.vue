<template>
  <div class="explore">
		<h1>اكتشف الاقسام و البرامج </h1>
		<div class="cards">
			<HomeCard v-for="(item, index) in list" :key="index" :data="item" />
		</div>
		<div class="more">
			<nuxt-link to="/departments">عرض الكل</nuxt-link>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			list: [
				{
					img: "/deptsIcons/0.jpg",
					title: "قسم الحاسبات",
					info: "هو احد اقسام الكلية و يعد اكثرهم تميزا",
					url: "/departments/0"
				},
				{
					img: "/deptsIcons/0.jpg",
					title: "قسم الحاسبات",
					info: "هو احد اقسام الكلية و يعد اكثرهم تميزا",
					url: "/departments/0"
				},
				{
					img: "/deptsIcons/0.jpg",
					title: "قسم الحاسبات",
					info: "هو احد اقسام الكلية و يعد اكثرهم تميزا",
					url: "/departments/0"
				},
			]
		}
	}
}
</script>