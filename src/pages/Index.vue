<template>
  <Layout>
    <About />
    <Experience />
    <Projects />
    <Skills />
    <Contact />
  </Layout>
</template>

<script>
import About from "../components/About";
import Experience from "../components/Experience";
import Projects from "../components/Projects";
import Skills from "../components/Skills";
import Contact from "../components/Contact";
export default {
  metaInfo: {
    title: "Hello, world!",
  },
  components: {
    About,
    Experience,
    Projects,
    Skills,
    Contact,
  },
};
</script>

<style>
.break-container {
  width: 100vw;
  position: relative;
  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
}
</style>
