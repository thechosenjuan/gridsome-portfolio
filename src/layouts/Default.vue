<template>
  <div class="layout px-5 mx-auto container">
    <header class="header">
      <strong>
        <g-link to="/">{{ $static.metadata.siteName }}</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Home</g-link>
      </nav>
    </header>
    <slot />
    <footer class="bg-gray-200 break-container px-16 py-10 h-full">
      <p class="inline-block">2020 ©</p>
      <div class="float-right -m-2 flex">
        <div class="mr-4 cursor-pointer" @click="handleGithubClick">
          <GithubIcon />
        </div>
        <div class="mr-4 cursor-pointer" @click="handleLinkedInClick">
          <LinkedinIcon />
        </div>
        <div class="cursor-pointer" @click="handleTwitchClick">
          <TwitchIcon />
        </div>
      </div>
    </footer>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>
<script>
import { GithubIcon, LinkedinIcon, TwitchIcon } from "vue-feather-icons";
export default {
  methods: {
    handleGithubClick: function() {
      window.open("https://github.com/thechosenjuan", "_blank");
    },
    handleLinkedInClick: function() {
      window.open("https://www.linkedin.com/in/juanfloresbarr/", "_blank");
    },
    handleTwitchClick: function() {
      window.open("https://twitch.tv/th3chosenjuan", "_blank");
    },
  },
  components: {
    GithubIcon,
    LinkedinIcon,
    TwitchIcon,
  },
};
</script>
<style>
body {
  font-family: -apple-system, system-ui, BlinkMacSystemFont, "Segoe UI", Roboto,
    "Helvetica Neue", Arial, sans-serif;
  margin: 0;
  padding: 0;
  line-height: 1.5;
  overflow-x: hidden;
}

.layout {
  /* max-width: 760px;
  margin: 0 auto; */
  /* padding-left: 20px;
  padding-right: 20px; */
}
.logo--github {
  width: 30px;
}

.logo--linkedin {
  width: 38px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
  height: 80px;
}

.nav__link {
  margin-left: 20px;
}
</style>
