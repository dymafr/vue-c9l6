<template>
  <small> {{ author.name }} - {{ author.birthdate }}</small>
</template>

<script setup lang="ts">
import { inject } from 'vue';
import { AuthorInterface } from './App.vue';

const { author, updateBirthday } =
  inject<Readonly<{ data: AuthorInterface; updateBirthday: () => void }>>(
    'author'
  )!;

setTimeout(() => {
  author.updateBirthday();
});
</script>

<style scoped lang="scss"></style>
