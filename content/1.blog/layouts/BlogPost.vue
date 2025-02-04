<script setup>
  const { next } = useContent()
    </script>
<template>
<div class="container">
  <div class="content">
    <slot />
  </div>
  <div v-if="next" class="next-link">
      <div> Read next post </div>
    <NuxtLink :to="next._path">
      {{ next.title }}
    </NuxtLink>
    <p>{{ next.description }}</p>
</div>
</template>
