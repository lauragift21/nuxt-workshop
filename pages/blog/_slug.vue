<template>
  <section class="container mx-auto">
    <h1 class="font-bold text-3xl mb-4 text-center">{{ article.title }}</h1>
    <nuxt-content :document="article" />
    <div class="lg:ml-64">
      <p class="font-bold">Written By:</p>
      <author :author="article.author" />
    </div>
  </section>
</template>

<script>
export default {
  async asyncData({ $content, params }) {
    const article = await $content("articles", params.slug).fetch();
    return {
      article,
    };
  },
};
</script>

<style>
.nuxt-content {
  max-width: 800px;
  margin: 0 auto;
}
.nuxt-content h2 {
  font-weight: bold;
  font-size: 28px;
}
.nuxt-content h3 {
  font-weight: bold;
  font-size: 22px;
}
.nuxt-content p {
  margin-bottom: 20px;
}
</style>