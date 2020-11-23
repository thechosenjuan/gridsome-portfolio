<template>
  <Layout>
    <About />
    <Experience />
  </Layout>
</template>

<script>
import About from "../components/About";
import Experience from "../components/Experience";
export default {
  metaInfo: {
    title: "Hello, world!",
  },
  components: {
    About,
    Experience,
  },
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
