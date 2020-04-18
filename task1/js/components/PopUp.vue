<template>
	<div v-show="showme">
		<div class="cover_all"></div>
		<div class="pop-up">

			<a @click="closeit">
				<img
					src="../../images/Exclusion26.jpg"
					class="close"
					alt="close it"
				/>
			</a>
			<section>
				<a href=""><img
						:src="icon_img"
						class="profile_img"
						alt="profile icon"
					/></a>
				<h3>{{title}}</h3>

				<p class="about">
					{{about}}
				</p>
				<button class="call-to-action">{{button_main}}</button>
				<button class="secondary-action">{{button_secondary}}</button>
			</section>
		</div>
	</div>
</template>

<script>
// ./../.
export default {
	data() {
		return {
			title: "Title example for two rows see the lines spacing",
			about:
				"Random text all users will see. You don’t know how long it is. you will see. You don’t know how long it is.",
			button_main: "Click me!",
			button_secondary: "Or here man",
			icon_img: "/icon.82bf699d.png",
			showme: true
		};
	},
	methods: {
		closeit() {
			this.showme = false;
		}
	}
};
</script>

<style lang="scss" scoped>
.pop-up {
	width: 314px;
	margin: 10px;
	height: 328px;
	border-radius: 16px;
	filter: drop-shadow(0 0 6px rgba(0, 0, 0, 0.4));
	background-color: #ffffff;
	z-index: 1;
}
.cover_all {
	background-color: rgba(78, 78, 78, 1);
	position: absolute;
	bottom: 0;
	left: 0;
	right: 0;
	top: 0;
}
.close {
	padding: 18px;
	position: absolute;
}
/* .profile_img {
         border: 2px solid #a70174;
        border-radius: 44px;
      }*/
section {
	text-align: center;
	padding: 40px;
	padding-top: 20px;
}
section h3 {
	max-lines: 2;
	/* font-family: "SF UI Display Bold", arial, tahoma; */
	font-size: 1.125em;
	color: #000;
	max-height: 60px;
	margin-top: 15px;
	margin-bottom: 20px;
	overflow: hidden;
	line-height: 1.4;
	text-overflow: ellipsis;
}
section p.about {
	height: 40px;
	font-size: 0.875em;
	text-overflow: ellipsis;
	overflow: hidden;
	color: #000;
	margin-bottom: 1.3em;
}
button {
	cursor: pointer;
}
.call-to-action {
	width: 240px;
	height: 44px;
	border-radius: 22px;
	filter: drop-shadow(1.908px 9.816px 11.5px rgba(144, 32, 113, 0.3));
	background-color: #a70174;
	font-size: 16px;
	color: #ffffff;
	font-weight: bold;

	text-align: center;
}

section .secondary-action {
	font-size: 13px;
	line-height: 16px;
	width: 240px;
	height: 44px;
	border-radius: 22px;
	color: #999999;
	border: none;
	text-align: center;
}
</style>