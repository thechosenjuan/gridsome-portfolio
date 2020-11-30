<template>
  <section class="text-gray-700 mt-8">
    <h2 class="text-center text-5xl font-bold">My Projects</h2>
    <div class="flex flex-wrap -m-4">
      <div class="p-4 md:w-1/2 lg:w-1/3">
        <div class="h-full border-2 border-gray-200 rounded-lg overflow-hidden">
          <g-image
            src="~/assets/images/pokedex_thumb.png"
            class="cursor-pointer"
            @click="openPokedexProject"
          />
          <div class="p-6">
            <h1
              class="title-font text-lg font-medium text-gray-900 mb-3 cursor-pointer"
              @click="openPokedexProject"
            >
              {{ projects[0].title }}
            </h1>
            <p
              class="leading-relaxed mb-3"
              v-html="projects[0].description"
            ></p>
          </div>
        </div>
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
      projects: [
        {
          thumbnail: "~/assets/images/pokedex_thumb.png",
          title: "StencilJS Pokedex",
          description:
            "This is based from the <a href='https://codepen.io/siliconunicorn/pen/VqoxXP' class='text-purple-500' target='_blank'>React Pokedex Project</a>. This was just a learning project to dive into StencilJS. ",
          url: "https://amazing-neumann-f5849a.netlify.app/",
        },
      ],
    };
  },
  methods: {
    openPokedexProject: function() {
      window.open(this.projects[0].url, "_blank");
    },
  },
};
</script>

<style></style>
