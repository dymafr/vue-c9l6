<template>
  <small> {{ author.name }} - {{ author.birthdate }}</small>
  <p>{{ api }}</p>
</template>

<script setup lang="ts">
import { inject } from 'vue';
import { AuthorInterface } from './App.vue';

const { author, updateBirthday } =
  inject<Readonly<{ data: AuthorInterface; updateBirthday: () => void }>>(
    'author'
  )!;
const api = inject('API_URL');

setTimeout(() => {
  updateBirthday();
}, 5000);
</script>

<style scoped lang="scss"></style>
