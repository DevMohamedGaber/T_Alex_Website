<template>
	<div id="department">
		<div class="header">
			<div class="img" :style="{backgroundImage: `url(${info.img})`}"></div>
			<div class="title">
				<div class="background">
					<div class="angle"></div>
					<div>
						<h1>{{ this.info.title }}</h1>
						<p>{{ this.info.preaf }}</p>
					</div>
				</div>
			</div>
			<div class="shadow"></div>
		</div>

		<article class="container">
			<section v-for="(section, index) in info.sections" :key="index">
				<h2>{{ section.title }}</h2>
				<p v-html="section.content"></p>
			</section>

			<div class="subjects" v-if="info.subjects && info.subjects.length > 0">
				<table>
					<caption>المواد المقررة</caption>
					<thead>
						<tr>
							<th>اسم المادة</th>
							<th>الترم</th>
							<th>الدرجة</th>
						</tr>
					</thead>
					<tbody>
						<tr v-for="(subject, index) in info.subjects" :key="index">
							<td>{{ subject.name }}</td>
							<td>{{ subject.term }}</td>
							<td>{{ subject.score }}</td>
						</tr>
					</tbody>
				</table>
			</div>
			
		</article>
		
	</div>
</template>
<script>
export default {
	head() {
		return {
			title: this.info.title
		}
	},
	async asyncData({ params, $axios })
	{
		const info = await $axios.$get(`http://localhost:3000/Database/Departments/${params.id}.json`)
		return { info }
	}
}
</script>