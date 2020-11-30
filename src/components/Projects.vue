<template>
  <section class="text-gray-700 mt-8">
    <h2 class="text-center text-5xl font-bold mb-4">My Projects</h2>
    <div class="flex flex-wrap -m-4">
      <div class="p-4 md:w-1/2 lg:w-1/3">
        <div class="h-full border-2 border-gray-200 rounded-lg overflow-hidden">
          <g-image
            src="~/assets/images/movix-project.png"
            class="cursor-pointer max-h-64"
            @click="openProject(projects[0].url)"
          />
          <div class="p-6">
            <h1
              class="title-font text-lg font-medium text-gray-900 mb-3 cursor-pointer"
              @click="openProject(projects[0].url)"
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
      <div class="p-4 md:w-1/2 lg:w-1/3">
        <div class="h-full border-2 border-gray-200 rounded-lg overflow-hidden">
          <g-image
            src="~/assets/images/pokedex_thumb.png"
            class="cursor-pointer max-h-64"
            @click="openProject(projects[1].url)"
          />
          <div class="p-6">
            <h1
              class="title-font text-lg font-medium text-gray-900 mb-3 cursor-pointer"
              @click="openProject(projects[1].url)"
            >
              {{ projects[1].title }}
            </h1>
            <p
              class="leading-relaxed mb-3"
              v-html="projects[1].description"
            ></p>
          </div>
        </div>
      </div>
      <div class="p-4 md:w-1/2 lg:w-1/3">
        <div class="h-full border-2 border-gray-200 rounded-lg overflow-hidden">
          <g-image
            src="~/assets/images/techcred-project.png"
            class="cursor-pointer max-h-64"
            @click="openProject(projects[2].url)"
          />
          <div class="p-6">
            <h1
              class="title-font text-lg font-medium text-gray-900 mb-3 cursor-pointer"
              @click="openProject(projects[2].url)"
            >
              {{ projects[2].title }}
            </h1>
            <p
              class="leading-relaxed mb-3"
              v-html="projects[2].description"
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
          title: "React Movie Catalog",
          description:
            "This project was developed in order to showcase an internal company tool that uses a graph DB. I was the lead Front End developer for the client side.",
          url: "https://movix.lab.base22.com/",
        },
        {
          thumbnail: "~/assets/images/pokedex_thumb.png",
          title: "StencilJS Pokedex",
          description:
            "This is based from the <a href='https://codepen.io/siliconunicorn/pen/VqoxXP' class='text-purple-500' target='_blank'>React Pokedex Project</a>. This was just a learning project to dive into StencilJS. ",
          url: "https://amazing-neumann-f5849a.netlify.app/",
        },
        {
          thumbnail: "~/assets/images/techcred-project.png",
          title: "Vue List Filter",
          description:
            "I made this for a State of Ohio <a href='https://techcred.ohio.gov/wps/portal/gov/techcred/home' target='_blank' class='text-purple-500'>agency</a>. It consists of list in which you can search/filter results by name and/or category.",
          url:
            "https://techcred.ohio.gov/wps/portal/gov/techcred/about/credential-list",
        },
      ],
    };
  },
  methods: {
    openProject: function(url) {
      window.open(url, "_blank");
    },
  },
};
</script>

<style></style>
