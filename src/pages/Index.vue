<template>
  <Layout>
    <About />
  </Layout>
</template>

<script>
import About from "../components/About";
export default {
  metaInfo: {
    title: "Hello, world!"
  },
  components: {
    About
  }
};
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>
