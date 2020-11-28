<template>
  <section class="text-gray-700">
    <h2 class="text-center text-5xl font-bold">Key Skills</h2>
    <div class="flex flex-wrap">
      <div
        v-for="(skill, index) in skills"
        :key="index"
        class="rounded-full py-3 px-6 bg-purple-500 text-white w-auto text-center h-12 m-3.5"
      >
        {{ skill }}
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Skills",
  data: function() {
    return {
      skills: [
        "Vue.JS",
        "Gridsome",
        "TailwindCSS",
        "JS",
        "HTML",
        "CSS",
        "Svelte",
        "Python",
        "ReactJS",
        "React Native",
        "Firebase",
        "PostgreSQL",
        "Flask",
        "Web Components",
        "StencilJS",
        "Netlify",
      ],
    };
  },
};
</script>

<style></style>
