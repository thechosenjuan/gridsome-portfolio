<template>
  <div class="layout px-5 py-12 mx-auto container">
    <header class="header">
      <strong>
        <g-link to="/">{{ $static.metadata.siteName }}</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">Home</g-link>
      </nav>
    </header>
    <slot />
    <footer class="bg-gray-200">
      <p class="inline-block">2020 ©</p>
      <div class="float-right -m-2">
        <g-image
          src="~/assets/images/github-logo.png"
          class="logo--github inline-block cursor-pointer"
          @click="handleGithubClick"
        />
        <g-image
          src="~/assets/images/linkedin-logo.png"
          class="logo--linkedin inline-block cursor-pointer"
          @click="handleLinkedInClick"
        />
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
export default {
  methods: {
    handleGithubClick: function() {
      window.open("https://github.com/thechosenjuan", "_blank");
    },
    handleLinkedInClick: function() {
      window.open("https://www.linkedin.com/in/juanfloresbarr/", "_blank");
    },
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
