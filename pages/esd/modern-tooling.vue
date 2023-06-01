<template>
  <h1>Modern Tooling</h1>
  <NotionRenderer :blockMap="data" prism />
</template>
<script setup>
const { $notion } = useNuxtApp(); // <--- plugins de nuxt...
const { data } = await useAsyncData("notion", () =>
  $notion.getPageBlocks("d621326fe9c3424f9c2777b8d4689d96")
);
</script>
<style lang="sass" scoped></style>
