<template>
  <Layout>
    <About />
    <Experience />
    <Projects />
    <Skills />
  </Layout>
</template>

<script>
import About from "../components/About";
import Experience from "../components/Experience";
import Projects from "../components/Projects";
import Skills from "../components/Skills";
export default {
  metaInfo: {
    title: "Hello, world!",
  },
  components: {
    About,
    Experience,
    Projects,
    Skills,
  },
};
</script>

<style></style>
