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
				<div class="space_img">
					<img
						src="../../images/close2.png"
						class="close_profile_photo"
						alt="close"
						@click="closeit"
					><img
						src="../../images/girl.jpg"
						class="profile_img"
						alt="profile icon"
					/>

				</div>
				<h3>{{title}}</h3>

				<p class="about">
					{{about}}
				</p>
				<div class="columns is-mobile">
					<div class="column is-half"><button class="secondary-action is-half">{{button_secondary}}</button></div>
					<div class="column is-half"><button class="call-to-action is-half">{{button_main}}</button></div>
				</div>

			</section>
		</div>
	</div>
</template>

<script>
// ./../.
export default {
	data() {
		return {
			title: "Title example for one row ",
			about:
				"Random text all users will see. You don’t know how long it is. you will see. You don’t know how long it is.",
			button_main: "Btn 1",
			button_secondary: "Btn 2",
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
$purple: #a70174;

.cover_all {
	background-color: rgba(78, 78, 78, 1);
	position: absolute;
	bottom: 0;
	left: 0;
	right: 0;
	top: 0;
}
.close_profile_photo {
	position: absolute;

	left: 116px;
	top: 32px;
	cursor: pointer;
}
.space_img {
	position: relative;
}
.pop-up {
	width: 314px;
	height: 267px;
	border-radius: 16px;
	filter: drop-shadow(0 0 6px rgba(0, 0, 0, 0.4));
	background-color: #ffffff;
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
	padding: 30px;
	padding-top: 20px;
}
section h3 {
	font-size: 1.125em;
	color: #000;
	max-height: 20px;
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
	width: 114px;
	height: 40px;
	border-radius: 20px;
	background-color: $purple;
	font-size: 16px;
	color: #ffffff;
	font-weight: bold;

	text-align: center;
}

.secondary-action {
	font-size: 16px;
	line-height: 16px;
	width: 114px;
	height: 40px;
	border-radius: 20px;
	background-color: #fafafa;
	border: 1px solid $purple;
	color: $purple;
	text-align: center;
}
@media only screen and (max-width: 480px) {
	.pop-up {
		width: 90%;
	}
}
</style>