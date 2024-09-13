<template>
	<!-- [Секция Main]: Main -->
	<section>
		<div class="container">
		
			<!-- [Секция Main]: Блок с картинкой -->
			<div class="main__img">
				<img src="@/assets/images/cats.svg" loading="lazy" width="10" height="10" alt="cats">
			</div>
			
		</div>
	</section>
</template>

<style>
.main__img {
	display: flex;
	align-items: center;
	justify-content: center;
	padding: 20px 0;
}

.main__img img {
	width: 100%;
	height: 100%;
}
</style>