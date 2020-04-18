<template>
	<div class="steps-to-earn">
		<h1>{{earn_revenue.length}} Steps to Earn revenue</h1>
		<div
			v-for="(value, name, index) in earn_revenue"
			:key="index"
			:name="name"
		>

			<div
				class="columns is-mobile"
				v-if="name!==0"
			>
				<div class="column ">
					<img
						src="/images/down-arrow.jpg"
						alt="down arrow"
						class="arrow"
					>
				</div>

			</div>

			<div class="columns is-mobile">
				<div class="column is-one-quarter"><img
						:src="value.images"
						alt="login"
						class="mobile"
					></div>
				<div class="column is-three-quarter right-desc">
					<span class="position">
						<span class="number_bakground"></span>
						<span class="number">{{ name+1 }}</span>

					</span>
					<h2>{{ value.title }} </h2>
					<p class="benefits">{{ value.description }} </p>
				</div>
			</div>
		</div>

		<div class="columns">
			<div class="column is-centered">
				<button @click="addstep">+</button>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	data() {
		return {
			earn_revenue: [
				{
					images: "/Login.9d1b61d1.jpg",
					// images: "/images/Login.jpg",

					title: "Create account",
					description:
						"Signing up is easy, it will take just a minute and then you are ready to receive gifts,compliments and money."
				},
				{
					images: "/photo-video.7be2cfbe.jpg",
					// images: "//images/photo-video.jpg",
					title: "Share your life",
					description:
						"Set prices and start chat with people, post pictures & vidos, make calls. Everything you do will earn ouy more."
				}
			]
		};
	},
	methods: {
		addstep() {
			this.earn_revenue.push({
				images: "/photo-video.7be2cfbe.jpg",
				title: "Some next title",
				description:
					"Set prices and start chat with people, post pictures & vidos, make calls. Everything you do will earn ouy more."
			}); // what to push unto the rows array?
		}
	}
	//
};
</script>

<style lang="scss" scoped>
.steps-to-earn {
	width: 355px;
	margin: 10px;
	height: auto;
	color: #000;
	background-color: #ffffff;
}
.right-desc {
	margin-left: 20px;
	margin-top: 10px;
	width: 320px;
}
h1 {
	font-family: "SF UI Display Bold", arial, tahoma;
	color: #000;
	font-size: 1.5rem;
	text-align: center;
	padding-bottom: 30px;
}
.position {
	position: relative;
	width: 30px;
	display: inline-block;
}
.number {
	font-family: "SF UI Display Bold", arial, tahoma;
	font-size: 1.4em;
	color: #ffffff;
	position: relative;
	left: -11px;
	top: -5px;
	background-color: transparent;
}
.number_bakground {
	position: absolute;
	left: 0px;
	z-index: 0;
	width: 34px;
	height: 34px;
	border-radius: 17px;
	filter: drop-shadow(1.935px 7.762px 11.5px rgba(144, 32, 113, 0.3));
	background-color: #a70174;
}
h2 {
	clear: right;
	display: inline-block;
	font-size: 1.375rem;
	position: relative;
	padding-left: 10px;
	top: 7px;
}
.benefits {
	margin-top: 20px;
	font-size: 0.875rem;
	line-height: 20px;
}
.mobile {
	min-width: 75px;
}
.arrow {
	margin: 0 auto;
	display: block;
}
button {
	margin: 0 auto;
	display: block;
	font-size: 2em;
	padding: 0.4em 0.7em;
	border-radius: 2em;
	cursor: pointer;
	margin-top: 2em;
}
@media only screen and (max-width: 480px) {
	.steps-to-earn {
		width: 90%;
	}
	h2 {
		font-size: 1.185rem;
	}
}
</style>