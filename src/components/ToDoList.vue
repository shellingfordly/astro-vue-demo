<script lang="ts" setup>
import { ref, watchEffect } from 'vue';

const list = ref(["睡觉", "吃饭"])
const something = ref("")

const add = () => (something.value && list.value.push(something.value));
</script>


<template>
	<input v-model="something" />
	<button @click="add()">ADD</button>

	<ul>
		<li v-for="item in list"> {{ item }}</li>
	</ul>
</template>
