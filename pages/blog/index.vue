<template>
  <section class="container mx-auto text-gray-900 body-font overflow-hidden">
    <h2 class="text-3xl font-bold text-center underline">Nuxt Blog</h2>
    <div class="container px-5 py-24 mx-auto">
      <div class="flex flex-wrap -m-12">
        <div
          class="p-12 md:w-1/2 flex flex-col items-start"
          v-for="article in articles"
          :key="article.id"
        >
          <span
            class="inline-block py-1 px-3 rounded theme-color text-white text-sm font-medium uppercase tracking-widest"
            >{{ article.tag }}</span
          >
          <h2
            class="sm:text-3xl text-2xl title-font font-medium text-gray-900 mt-4 mb-4"
          >
            {{ article.title }}
          </h2>
          <p class="leading-relaxed mb-8">
            {{ article.description }}
          </p>
          <div
            class="flex items-center flex-wrap pb-4 mb-4 border-b border-gray-200 mt-auto w-full"
          >
            <nuxt-link
              :to="`blog/${article.slug}`"
              class="text-green-800 inline-flex items-center"
              >Learn More
              <svg
                class="w-4 h-4 ml-2"
                viewBox="0 0 24 24"
                stroke="currentColor"
                stroke-width="2"
                fill="none"
                stroke-linecap="round"
                stroke-linejoin="round"
              >
                <path d="M5 12h14"></path>
                <path d="M12 5l7 7-7 7"></path>
              </svg>
            </nuxt-link>
          </div>
          <a class="inline-flex items-center">
            <author :author="article.author" />
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  async asyncData({ $content }) {
    const articles = await $content("articles").fetch();
    return {
      articles,
    };
  },
};
</script>

<style>
.theme-color {
  background: #3b8070;
}
</style>