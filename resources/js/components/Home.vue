<template>
	<div class="home" >
		<component v-for="(component, index) in json"
				   :key="'component'+index"
				   :is="component[1].basename"
				   v-bind="component[1].props">
		</component>
	</div>
</template>

<script>
	import componentsHome from '../../../customization/home.json';

	export default {
		data(){
			return {
				json: Object.entries(componentsHome)
			}
		}
	}
</script>
