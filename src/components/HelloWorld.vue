<script setup lang="ts">
import { ref, defineProps } from "vue";

interface Props {
  msg?: string;
  name: string;
}

const props = defineProps<Props>();

const localData = ref<string>("looo");

const localFun = (parameter: string) => {
  localData.value = parameter;
};
</script>

<template>
  <h1>{{ props.name }}</h1>
  <h3>{{ props.msg }}</h3>
  <p>{{ localData }}</p>
  <p @click="localFun('oool')">Click!</p>
</template>

<style scoped></style>
