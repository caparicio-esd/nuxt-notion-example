<template>
  <h1>PostCss and Tailwind</h1>
  <NotionRenderer :blockMap="data" prism />
</template>
<script setup>
const { $notion } = useNuxtApp(); // <--- plugins de nuxt...
const { data } = await useAsyncData("notion", () =>
  $notion.getPageBlocks("26f526ef38ec4397a7025fa30eae5cdf")
);
</script>
<style lang="sass" scoped></style>
