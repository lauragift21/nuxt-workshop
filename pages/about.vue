<template>
  <section class="container ml-40 my-4 my-12">
    <h1 class="font-bold">About Me</h1>
    <h2 class="text-4xl">Hi there! I'm Gift Egwuenu</h2>
    <p class="text-2xl">I'm a {{ role }} at {{ work }}.</p>
    <p class="text-2xl">
      I'm currently based in {{ location }} and I enjoy watching Netflix and
      Photography.
    </p>
  </section>
</template>

<script>
export default {
  data() {
    return {
      work: "Passionate People",
      role: "Frontend Developer Consultant",
      location: "Lagos",
    };
  },
};
</script>

<style scoped>

</style>