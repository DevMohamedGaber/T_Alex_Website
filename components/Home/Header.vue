<template>
	<div class="header">
		<div class="background">
			<img src="/header.webp" alt="header" />
			<div class="overlay"></div>
			<h1>الـكلية التكنولـــوجية بالاسكندرية</h1>
			<p>الرائد الاكاديمي للمجالات الصناعية و التكنولوجية الحديثة</p>
		</div>

		<div class="container">
			<ul class=" links">
				<li>
					<nuxt-link to="/location">
						<img src="/Icons/location.png" alt="">
						<br />
						<span>زرنـا</span>
					</nuxt-link>
				</li>
				<li>
					<nuxt-link to="/contacts">
						<img src="/Icons/contact.png" alt="">
						<br />
						<span>تواصـل</span>
					</nuxt-link>
				</li>
				<li>
					<nuxt-link to="/blogs">
						<IconsNews />
						<br />
						<span>اخبـار</span>
					</nuxt-link>
				</li>
				<li>
					<nuxt-link to="/events">
						<img src="/Icons/events.png" alt="" />
						<br />
						<span>احـداث</span>
					</nuxt-link>
				</li>
			</ul>
		</div>
	</div>
</template>