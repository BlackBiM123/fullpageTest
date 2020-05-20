<template>
	<div>

		<full-page ref="fullpage" :options="options">
			<div class="section main-section">
				1
				<button @click="testAction = !testAction">Test Action Button</button>
				<div v-if="testAction">Hidden block</div>
			</div>
			<div class="section player-section">
				2
			</div>
			<div class="section characteristics-section">
				3
			</div>
			<div class="section fp-auto-height">
				<div style="height: 300px;display:flex; justify-content: center;align-items: center;font-size:40px;"class="inner-footer">
					Footer
				</div>
			</div>
		</full-page>
	</div>
</template>

<script>


	export default {
		name: "ModelPage",
		data() {
			return {
				testAction:false,
				options: {
					licenseKey: 'C0E668ED-D0884799-98266D1B-35FA0817',
					navigation: true,
					verticalCentered: false,
					anchors: ['main', 'player', 'info',  'footer'],
					sectionsColor: ['#41b883', '#ff5f45', '#0798ec'],
					responsiveHeight: 0,
					navigationTooltips: ['anchor1', 'anchor2', 'anchor3'],
				},


			}
		},
	}
</script>

<style scoped>
	.section{
		display:flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
	}
</style>
