<template>
  <div class="p-4 md:w-1/3">
    <div class="h-full border-2 border-gray-200 rounded-lg overflow-hidden">
      <img :src="thumbnail" />
      <div class="p-6">
        <h1 class="title-font text-lg font-medium text-gray-900 mb-3">
          {{ title }}
        </h1>
        <p class="leading-relaxed mb-3">
          {{ description }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Card",
  props: ["thumbnail", "title", "description"],
};
</script>

<style></style>
