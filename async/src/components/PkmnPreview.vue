<template>
  <div class="container">
    <h1>{{ pokemon.name }}</h1>
  </div>
</template>

<script>
export default {
  name: "PkmnPreview",
  props: ["pokemon"],
};
</script>

<style>
</style>