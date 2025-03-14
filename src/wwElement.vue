<template>
	<div class="css-marker" v-if="visible">CSS Loaded</div>
</template>

<script setup>
import { computed } from "vue";

const visible = computed(() => {
	return wwLib && wwLib.env && wwLib.env === "development";
});
</script>

<style>
:root {
	--theme-blue: #2794eb;
	--theme-green1: #bff8d4;
	--theme-green2: #47d6b6;
	--theme-green3: #17b3c1;
	--theme-placeholder-color: #c5c5c5;
}
</style>

<style lang="scss" scoped>
.css-marker {
	position: absolute;
	top: 0;
	left: 0;
	color: black;
	background-color: var(--theme-green3) !important;
	z-index: 100 !important;
}
</style>
