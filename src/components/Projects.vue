<template>
  <section class="text-gray-700 mt-8">
    <h2 class="text-center text-5xl font-bold">My Projects</h2>
    <div class="container px-5 py-12 mx-auto">
      <div class="flex flex-wrap -m-4">
        <Card v-for="(project, index) in projects" :key="index" />
      </div>
    </div>
  </section>
</template>

<script>
import Card from "./Card";
export default {
  name: "Projects",
  components: {
    Card,
  },
  data: function() {
    return {
      projects: [1, 2, 3],
    };
  },
};
</script>

<style></style>
