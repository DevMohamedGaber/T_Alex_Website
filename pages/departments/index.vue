<template>
	<div id="departments">
		<div class="container">
			<h1>اقسام المعهد</h1>
			<p>يوجد بالمعهد العديد من الاقسام الميكانيكية, الكهربية و المعمارية</p>
			<div class="cards">
				<HomeCard v-for="(item, index) in list" :key="index" :data="item" />
			</div>
			<div class="more">
				<nuxt-link to="/departments">عرض الكل</nuxt-link>
			</div>
		</div>
	</div>
</template>