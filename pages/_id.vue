<template>
  <section class="container mx-auto">
    <h2 class="text-4xl">Get Your GitHub Profile</h2>
    <div class="my-4 flex items-center">
      <img
        :src="data.avatar_url"
        class="rounded-full w-1/4 mb-6"
        alt="profile image"
      />
      <div class="px-10">
        <h2 class="text-3xl font-bold">{{ data.name }}</h2>
        <p class="text-xl text-gray-900">{{ data.owner }}</p>
        <a class="pt-2 text-xl underline" :href="data.blog">{{ data.blog }}</a>
        <h2 class="pt-2 text-xl">{{ data.bio }}</h2>
        <h2 v-if="data.company" class="pt-2 text-xl font-bold">💼 {{ data.company }}</h2>
        <span class="font-bold text-xl">Followers: {{ data.followers }}</span>
        <span class="font-bold text-xl">Following: {{ data.following }}</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  async asyncData({ params, $http }) {
    const data = await $http.$get(`https://api.github.com/users/${params.id}`);
    return { data };
  },
};
</script>

<style>
</style>