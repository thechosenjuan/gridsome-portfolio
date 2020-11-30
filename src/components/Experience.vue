<template>
  <div class="bg-gray-200 py-16 break-container md:px-40 sm:px-4 px-4 lg:px-80">
    <div
      v-for="(event, index) in timelineItems"
      :key="index"
      class="relative m-4"
    >
      <p class="font-bold absolute sm:-left-36 sm:right-0 right-10">
        {{ event.dateRange.from.month }} - {{ event.dateRange.from.year }}
      </p>
      <p>{{ event.location }}</p>

      <p class="inline-block italic">{{ event.company }}</p>
      -
      <p class="inline-block font-bold">{{ event.title }}</p>

      <p class="text-justify">{{ event.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Experience",
  data: function() {
    return {
      timelineItems: [
        {
          dateRange: {
            from: {
              month: "Sep.",
              year: "2019",
            },
            to: {
              month: "",
              year: "",
              current: true,
            },
          },
          title: "Enterprise Web Developer",
          company: "Base22",
          location: "Columbus, OH",
          description:
            "My main focus is to develop and maintain intranets for the State of Ohio and its diverse agencies. I mostly work with Vue.JS and Tailwind CSS. Amongst the sites I've built, I developed the main site that the State of Ohio is using as central information hub during the coronavirus pandemic",
          showcase: "https://coronavirus.ohio.gov",
        },
        {
          dateRange: {
            from: {
              month: "Jul.",
              year: "2017",
            },
            to: {
              month: "Aug.",
              year: "2019",
              current: false,
            },
          },
          title: "Enterprise Web Developer",
          company: "Base22",
          location: "Monterrey, MX",
          description:
            "As a Front End Developer, I was tasked with developing and maintaing intranets for different clients like CEMEX, UPS and the State of Ohio. I also gained experience as instructor by facilitating and providing a course on Web Components with Stencil.",
        },
        {
          dateRange: {
            from: {
              month: "Jan.",
              year: "2017",
            },
            to: {
              month: "Jul.",
              year: "2017",
              current: false,
            },
          },
          title: "Web Dev. Intern",
          company: "Base22",
          location: "Monterrey, MX",
          description:
            "During my time as an intern, I was tasked with translating company proprietary JS components to Vue.JS.",
        },
      ],
    };
  },
};
</script>
