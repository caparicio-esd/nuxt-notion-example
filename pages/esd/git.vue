<template>
  <h1>Gitd</h1>
  <NotionRenderer :blockMap="data" prism />
</template>
<script setup>
const { $notion } = useNuxtApp(); // <--- plugins de nuxt...
const { data } = await useAsyncData("notion", () =>
  $notion.getPageBlocks("2da7c5189e974ea89ae88bab881da3b3")
);
</script>
<style lang="sass" scoped></style>
