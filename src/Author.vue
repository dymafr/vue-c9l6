<template>
  <small> {{ author.name }} - {{ author.birthdate }}</small>
</template>

<script setup lang="ts">
import { inject } from 'vue';
import { AuthorInterface } from './App.vue';

const author = inject<AuthorInterface>('author')!;
</script>

<style scoped lang="scss"></style>
