<template>
  <div>
    <Navbar />
    <Content />
    <Footer />
  </div>
</template>

<style>
::-webkit-scrollbar {
  width: 5px;
}
::-webkit-scrollbar-thumb {
  background: var(--cyan);
  border-radius: 8px;
}

::-webkit-scrollbar-track {
  background: rgb(231, 231, 225);
}
</style>

<script>
import Navbar from "@/components/Navbar.vue";
import Footer from "@/components/Footer.vue";
import Content from "@/components/Content.vue";
export default {
  components: {
    Navbar,
    Footer,
    Content,
  },
};
</script>
