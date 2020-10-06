<template>
  <section class="container mx-auto">
    <h1 class="font-bold text-3xl">{{ article.title }}</h1>
    <nuxt-content :document="article" />
    <p class="font-bold">Written By:</p>
    <author :author="article.author" />
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
.nuxt-content-highlight {
  max-width: 700px;
}
</style>